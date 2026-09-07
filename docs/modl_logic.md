# Model Logic

## Business objective

Build an annual procurement and raw material cost model for a fictional
gazpacho manufacturer.

The model connects production planning with raw material requirements,
purchasing decisions, purchase prices, product cost and waste control.

## Model flow

Production Plan
→ Ingredient Master / BOM
→ Raw Material Requirements
→ Purchasing Plan
→ Weighted Average Purchase Price
→ Raw Material Cost
→ Finished Product Cost
→ Waste Control
→ KPIs

## Core principles

- Ingredient master data is separated from transactional purchasing data.
- Raw material requirements are calculated from production volume, recipe
  percentage and expected waste.
- Required purchase quantity and actual purchased quantity are tracked separately.
- Up to two purchase quantities and prices can be recorded per ingredient and month.
- Purchase prices are calculated using a weighted average.
- Expected waste is compared with actual waste.
- Waste deviations greater than ±1% of monthly finished production trigger an alert.
- Manufacturing, packaging and other variable costs remain manual inputs.