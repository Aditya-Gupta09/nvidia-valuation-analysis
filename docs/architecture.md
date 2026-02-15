# Architecture — Deal Analysis & Valuation Engine

## Objective
Design a modular pipeline that supports:
1. Data ingestion and cleaning
2. Financial normalization and L3 model generation
3. Valuation engines (DCF, comps, simple transaction adjustments)
4. Report generation (memo PDF, screenshots)
5. Optional web UI for browsing valuations

## Components

### 1) Data layer
- `datasets/raw/`: source CSV exports (manual or script-driven)
- `datasets/processed/`: cleaned, validated CSVs for modeling

### 2) Modeling layer (Excel + optional Python)
- Excel L3 models live in `models/` (primary artifact)
- `models/templates/` holds reusable templates
- Future `src/` will host Python routines to generate key blocks (WACC, FCFF, sensitivity tables)

### 3) Valuation layer
- DCF engine:
  - FCFF calculation, discounting, terminal value (Gordon & exit multiple)
- Comparable valuation:
  - Peer selection, multiples table, implied range

### 4) Reporting layer
- `reports/` holds memo PDF and template
- `screenshots/` contains model visuals used in memo

### 5) Automation & testing (future)
- `src/` Python modules for repeatable WACC/DCf computations
- `tests/` unit tests to validate calculations

## Data flow (high-level)
1. Export raw financials → `datasets/raw/`  
2. Clean & normalize → `datasets/processed/cleaned_financials.csv`  
3. Open L3 Excel model → link to processed data or copy values  
4. Run valuation → produce sensitivity screenshots & memo draft  
5. Commit artifacts to `reports/` and `screenshots/`

## Diagram suggestion
Create a simple diagram (draw.io or Mermaid) showing arrows:
`datasets/raw` → `datasets/processed` → `models/L3` → `reports` → `screenshots`
