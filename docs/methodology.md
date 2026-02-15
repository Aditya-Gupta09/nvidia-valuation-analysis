# Methodology — Data cleaning and modeling rules

## General principles
- Keep historicals faithful to filings; isolate non-recurring items in an `Adjustments` section.
- Use driver-based forecasting (volume × price or segment growth) where available.
- Keep formulas transparent — no hidden hard codes.

## Historical cleaning
- Remove one-time gains/losses (e.g., asset sale, restructuring).
- Normalize tax rate: use average or management guidance, and document.
- Capitalize vs expense: follow IFRS/US GAAP used by the company.

## Working capital
- Compute NWC as: `Receivables + Inventory - Payables`.
- Use DSO / DIO / DPO where possible; otherwise use % of revenue.

## CapEx & Depreciation
- CapEx as % of revenue (or guidance)
- Depreciation linked to historical PP&E schedule

## Leases & ROU assets
- If advanced: capitalize operating leases (IFRS 16 / ASC 842) and adjust debt/EBITDA accordingly.

## Non-core items
- Present adjustments tab listing each normalization (amount, period, explanation).

## Validation checks
- Income statement, balance sheet and cash flow must reconcile.
- Free cash flow reconciling to cash change (after financing) is required.
- Sensitivity checks: monotonic behaviour when changing drivers.
