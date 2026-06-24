# Deployment

ThreatQuest Cyber Hunt is prepared for local development and live hosting without changing the core application structure.

## Recommended runtime

Flask web/API service with persistent disk for live data.

## Local run

`pip install -r requirements.txt`

`python backend/app.py`

## Environment variables

Set `SECRET_KEY`; use the persistent disk path for SQLite or configure Postgres later.

## Production notes

- Keep secrets in the hosting provider's environment settings, not in source control.
- Use the included `.env.example` files as a checklist only.
- For AI/model projects, choose a plan with enough memory for model loading and inference.
- For frontend/backend projects, deploy the backend first, then point the frontend API base URL to the live backend URL if the frontend is not served by the same process.
