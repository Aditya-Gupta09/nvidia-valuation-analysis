# Roadmap & Milestones

## Phase 1 — MVP (Complete / 1–2 weeks)
- Finalise L3 Excel model for case study (NVIDIA)
- Produce 1-page investment memo
- Create README, docs, and datasets exports
- Commit screenshots (sensitivity + valuation bridge)

## Phase 2 — Reproducibility (2–4 weeks)
- Extract L3 template
- Add cleaned dataset CSVs
- Add small Python utilities for WACC & sensitivity tables

## Phase 3 — Multi-company & automation (4–8 weeks)
- Build `src/` modules to ingest CSVs and produce valuation tables
- Add unit tests and CI (GitHub Actions)
- Batch-run valuations for 3 sample tickers

## Phase 4 — Presentation layer (optional)
- Minimal web UI to browse saved valuations (Flask / Streamlit)
- Add export to PDF for memo generation

## Milestones & deliverables
- M1: Interview-ready Nvidia package (Excel + memo + README) — target: this week  
- M2: Template L3 model & cleaned dataset — target: +1 week  
- M3: Basic Python DCF & WACC scripts + tests — target: +3 weeks
