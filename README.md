# Multimodal Construction Intelligence Platform

Skill Wallet Capstone Project 1: a database-free Streamlit decision-support dashboard for construction safety, crack screening, project planning, valuation, and weather-aware site protocols.

## Run locally

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```

The app starts in deterministic demonstration mode when no Gemini key is provided. To enable multimodal Gemini analysis, enter a key in the sidebar or set `GEMINI_API_KEY` before starting Streamlit. The key is not written to disk.

## Deploy on Streamlit Community Cloud

Set the app entry point to `app.py`, keep `requirements.txt` at the repository root, and optionally add `GEMINI_API_KEY` under the deployment's Secrets settings. Users can still use demonstration mode without a secret.

## Modules

- **Safety & PPE:** image upload, PPE checklist, hazards, corrective remedies, structured JSON download.
- **Crack Diagnostics:** defect classification, indicative crack width, causes, repairs, urgency, and JSON download.
- **Planning & Valuation:** INR project budget, incurred CAPEX, market valuation, milestone, and material indicators.
- **Daily Assistant:** weather-specific controls and a multi-turn session chatbot.

AI results are screening aids and do not replace competent-person inspections, structural engineering design, approved method statements, or quantity-surveyor estimates.
