# ForensiAI

AI-powered digital forensics dashboard (capstone project) for **local SOC-style demonstrations**.  
ForensiAI ingests **macOS Unified Logs** (Windows log concepts supported for future work), applies **AI-style heuristic risk scoring**, and generates **supervisor-friendly PDF/CSV reports**.

## Website
https://alsowaidi98.github.io/ForensiAI/

## Key components
- **Analyst dashboard (Streamlit)**: `app.py`  
- **Project Manager console (Streamlit)**: `pm_console.py`  
- **Ingestor scripts**: parse + normalise logs into CSV/SQLite  
- **Reporting**: PDF/CSV exports + activity logging  
- **Architecture diagram**: `website/assets/forensiai-architecture.svg`

## Architecture
See the diagram on the Docs page or in: `website/assets/forensiai-architecture.svg`

## Quick start (macOS)
```bash
git clone https://github.com/Alsowaidi98/ForensiAI.git
cd ForensiAI
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py

# ForensiAI

AI-powered digital forensics dashboard (capstone project). Ingests macOS Unified Logs (with Windows concepts planned), applies AI-style risk scoring, and generates supervisor-friendly PDF/CSV reports.

## Website
https://alsowaidi98.github.io/ForensiAI/

## Components
- Analyst dashboard (Streamlit): `app.py`
- Project Manager console (Streamlit): `pm_console.py`
- macOS Unified Log ingestor scripts → CSV/SQLite state
- PDF/CSV reporting + analyst activity logging

## Quick start (macOS)
```bash
git clone https://github.com/Alsowaidi98/ForensiAI.git
cd ForensiAI
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# start ingestion (choose one)
./start_forensiai.sh
# or:
python ingest_macos_unifiedlog.py

# run dashboards
streamlit run app.py
# (optional PM console)
streamlit run pm_console.py
