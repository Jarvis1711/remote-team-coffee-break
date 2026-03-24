# Remote Team "Coffee Break"

## Solution Summary
Production-ready domain application.

This Phase-2 implementation is a domain-ready, deployable web application for **Logistics & Operations** workflows.

## Core Capabilities
- Responsive dashboard with KPI cards and recent activity table
- Domain record lifecycle with full CRUD (web + API)
- Dynamic schema fields tailored to this use case
- Status pipeline: `scheduled, active, delayed, completed`
- Docker + Gunicorn deployment assets, CI checks, and Pytest tests

## Domain Model
- Primary entity: **Remote Team Operation**
- Collection: **Remote Team Operations**
- Dynamic fields:
- Location (`location` / text)
- Capacity (`capacity` / number)
- Execution Notes (`execution_notes` / textarea)

## Operational Workflow
1. Plan operation
2. Dispatch resources
3. Monitor execution
4. Close operation

## API
- `GET /api/health`
- `GET /api/schema`
- `GET /api/records`
- `POST /api/records`
- `GET /api/metrics`

## Run Locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Docker Run
```bash
docker compose up --build
```

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
