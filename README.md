# E9 — Lab Report Rubric Scorer

Evidence-backed grading. One specialist AI agent per rubric criterion, cited evidence quotes, deterministic weighted totals in Python.

## Structure

```
e9/
├── backend/          # FastAPI + Groq agents
├── frontend/         # Dashboard + auth (static)
├── landing/          # Marketing page
├── migrations/       # Alembic
├── alembic.ini
└── Procfile
```

## Quick start (local)

```bash
cd backend
pip install -r requirements.txt
export GROQ_API_KEY=your_key
export JWT_SECRET_KEY=change-me
uvicorn main:app --reload --port 8000
```

Open `frontend/login.html` in browser (or serve the frontend folder).

## Deploy

- Backend → Railway (Procfile already points to `--app-dir backend`)
- Frontend → Vercel/Netlify (set root to `frontend`)
- Landing → separate static host or same

Update `API_BASE_URL` in the frontend HTML files after backend is live.
