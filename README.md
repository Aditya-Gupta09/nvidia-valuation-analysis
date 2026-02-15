# Nvidia-Valuation-Analysis-Model

# Deal Analysis & Valuation Engine

**Status:** Active development — single-company case study (NVIDIA) with L3 financial model and investment memo; roadmap to automation and multi-company support.

> Case study: :contentReference[oaicite:1]{index=1}

---

## Project overview

This repository contains a structured financial modelling and valuation framework designed to produce defensible, reproducible valuations for publicly listed companies. The current scope includes:

- Cleaned historical financials (3 years)
- 5-year driver-based projections
- L3 Excel model (IS / BS / CF linked)
- FCFF DCF valuation with explicit WACC
- Two terminal value approaches (Gordon growth, exit multiple)
- Comparable company screening and implied valuation
- One-page investment memo template
- Documentation and reproducible dataset layout

**Goal:** produce an interview-ready valuation package per company and evolve into a reusable valuation engine.

---

## Contents

```
deal-analysis-valuation/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── architecture.md
│   ├── methodology.md
│   ├── valuation-framework.md
│   └── roadmap.md
│
├── models/
│   ├── Company_Valuation_Model.xlsx
│   └── templates/
│       └── L3_Model_Template.xlsx
│
├── reports/
│   ├── Investment_Memo_NVIDIA.pdf
│   └── memo_template.md
│
├── datasets/
│   ├── raw/
│   │   ├── nvidia_historical_financials.csv
│   │   └── nvidia_market_data.csv
│   └── processed/
│       └── cleaned_financials.csv
│
├── comps/
│   ├── comps_data.csv
│   └── comps_methodology.md
│
├── screenshots/
│   ├── dcf_sensitivity.png
│   └── valuation_bridge.png
│
└── src/ (planned)
```



---

## Quickstart (how to inspect)

1. Open `models/Company_Valuation_Model.xlsx` to review assumptions and projections.  
2. Review `reports/memo_template.md` for the one-page memo layout.  
3. See `docs/architecture.md` for system design and `docs/methodology.md` for modelling rules.

---

## How to contribute / personal notes

- I am the primary author and will add a production automation layer (`src/`) after the model and documentation are finalised.  
- Files under `datasets/raw/` are source exports — do not edit in place. Place cleaned outputs in `datasets/processed/`.

---

## Data sources & attribution

- Company filings (investor relations / EDGAR)  
- Yahoo Finance (market data, beta)  
- Publicly available peer financials (manual compilation)

---

## License & disclaimer

See `LICENSE`.  
This project is for educational and demonstrative purposes only and is **not** investment advice.
