# CareAssist — Healthcare AI Chatbot Prototype

This is a classroom demonstration prototype based on the Business Analysis 3.2 project, “AI Integration Into Healthcare”.

## Features
- Web chat interface
- Local SQLite database
- Search fictional patient records by demo ID (P1001, P1002, P1003)
- Search a small medical-reference index (asthma, hypertension, diabetes, drug safety)
- Basic rule-based natural-language matching
- Safety notice and emergency escalation message

## Run it
1. Install Python 3.10 or newer.
2. Open a terminal in this folder.
3. (Optional but recommended) Create and activate a virtual environment.
4. Install dependencies: `python -m pip install -r requirements.txt`
5. Start the app: `python app.py`
6. Open `http://127.0.0.1:5000` in your browser.

The SQLite database is created and seeded automatically on first startup.

## Example questions
- `Search patient P1001`
- `Summarize patient P1002`
- `What allergy risks are recorded for P1001?`
- `Find references about blood pressure`
- `Find references about asthma`
- `Search drug safety`

## Important limitations
- All patient records are fictional examples.
- The chatbot uses keyword matching and retrieval, not a trained medical AI model or an LLM.
- It does not connect to a hospital EHR, FHIR API, clinical trial database, or live medical literature service.
- Medical reference entries are a small demo index; open the links to verify current guidance.
- Do not enter real patient data. Do not use this prototype for diagnosis, treatment, prescribing, or clinical decisions.
- A real deployment would require institutional approval, privacy/security controls, access control, audit logs, validated clinical models, data-quality checks, and integration testing.
