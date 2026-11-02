# HealthCareAI - Healthcare Admissions Analysis and Condition Prediction

Dataset: `healthcare_dataset.csv` (55,500 hospital admissions, 15 columns).

## Files
```
HealthCareAI/
├── healthcare_dataset.csv   the dataset
├── train.py                 STEP 1  clean, explore, train + compare models
├── test.py                  STEP 2  evaluate on unseen patients, build results/report.html
├── predict.py               STEP 3  predict (demo / CSV batch / interactive)
├── app.py                   web app (dashboard, predict, model results)
├── requirements.txt
└── README.md
```
Generated: `model.pkl`, `healthcare_clean.csv`, `train_split.csv`, `test_split.csv`, `results/` (graphs, tables, report.html).

## Run
```bash
pip install -r requirements.txt
python train.py
python test.py
python predict.py                  # demo   | python predict.py file.csv | python predict.py --interactive
streamlit run app.py
```
Open `results/report.html` for every table and graph in one page.

## Method
- Cleaning: names fixed, duplicates and near-duplicates removed, negative bills removed, Length of Stay added.
- Split 80/20 **by patient** so the same person is never in both train and test.
- Models compared: baseline, Logistic Regression, Decision Tree, Random Forest (tuned with grouped cross-validation).

## Result
Test accuracy is about 16.6 %, equal to chance for 6 classes (baseline 16.4 %). The Random Forest
memorises the training data (65 % train vs 17 % test) but learns nothing that generalises, because
the dataset is synthetic and its fields are independent of the condition. The analysis, tables
and graphs are valid; the prediction is a demonstration only, not a diagnosis tool.

