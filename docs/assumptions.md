# Model Assumptions

## Purpose

This document summarises the main business and modelling assumptions used in the Gazpacho Procurement & Raw Material Cost Model.

All assumptions and data are fictional and have been created exclusively for portfolio and learning purposes. They do not represent operational, purchasing, production or cost data from any real company.

## Model Period

- Model year: 2026
- Planning frequency: monthly
- Reference annual production scenario: 1,200,000 litres
- January production scenario: 100,000 litres
- February to December production volumes remain blank for manual planning.

The annual reference scenario is informational and does not automatically populate monthly production.

## Production Assumptions

- Finished-product density: 1.00 kg/L
- Production is entered in litres.
- Raw material requirements are calculated in kilograms.
- The model assumes that recipe percentages represent the net material incorporated into the finished product.
- Expected waste is applied separately to estimate the gross quantity that must be purchased.

## Recipe / BOM

| Ingredient | Recipe % | Expected Waste % |
|---|---:|---:|
| Pear Tomato | 70.3% | 8.0% |
| Cucumber | 12.2% | 12.0% |
| Green Pepper | 7.3% | 15.0% |
| Onion | 4.4% | 10.0% |
| Garlic | 0.8% | 8.0% |
| Extra Virgin Olive Oil | 2.6% | 0.5% |
| Sherry Vinegar | 1.3% | 0.5% |
| Salt | 0.7% | 0.0% |
| Lemon Juice | 0.4% | 2.0% |
| **Total** | **100.0%** | |

Recipe percentages and expected waste rates are fictional modelling assumptions.

## Raw Material Requirement

Net raw material requirement is calculated from finished production volume and recipe percentage:

`Net Requirement kg = Production L × Density kg/L × Recipe %`

Gross purchase requirement includes expected waste:

`Required Purchase kg = Net Requirement kg / (1 - Expected Waste %)`

Expected waste is therefore:

`Expected Waste kg = Required Purchase kg - Net Requirement kg`

## Purchasing Assumptions

- Purchase unit of measure: kg
- Currency: EUR
- Up to two purchase quantities and prices can be recorded per ingredient and month.
- Purchase prices are manual inputs.
- January Purchase 1 quantities are prefilled with the calculated required purchase quantity for demonstration purposes.
- Future purchase quantities and prices remain blank for manual input.
- Required purchase quantity and actual purchased quantity are tracked separately.

When two purchases are recorded, the model calculates a weighted average purchase price rather than a simple arithmetic average.

## Purchase Control

Purchase variance is calculated as:

`Purchase Variance kg = Actual Purchased kg - Required Purchase kg`

Purchase coverage is calculated as:

`Purchase Coverage % = Actual Purchased kg / Required Purchase kg`

These KPIs provide visibility over under-purchasing and over-purchasing relative to calculated material requirements.

## Waste Control

Actual waste is a manual input.

The model compares actual waste with expected waste:

`Waste Variance kg = Actual Waste kg - Expected Waste kg`

The default alert threshold is **±1.00% of monthly finished production**.

Waste status is classified as:

- `OK` when the deviation remains within the threshold.
- `WARNING – EXCESS WASTE` when actual waste exceeds the upper threshold.
- `WARNING – BELOW EXPECTED WASTE` when actual waste falls below the lower threshold.

The threshold is editable in the Assumptions sheet.

## Cost Assumptions

Raw material spend is based on actual recorded purchase quantities and prices.

Raw material cost per litre is calculated as:

`Raw Material Cost €/L = Monthly Raw Material Spend € / Finished Production L`

The following costs remain manual inputs:

- Manufacturing variable cost €/L
- Packaging cost €/L
- Other variable cost €/L

Total product cost is calculated as:

`Total Product Cost €/L = Raw Material Cost €/L + Manufacturing Variable Cost €/L + Packaging Cost €/L + Other Variable Cost €/L`

## Scope Limitations

Version 1 does not model:

- inventory levels;
- opening or closing stock;
- safety stock;
- supplier lead times;
- minimum order quantities;
- supplier capacity;
- logistics costs;
- production seasonality;
- demand forecasting;
- fixed manufacturing overhead;
- selling price;
- gross margin.

As a result, required purchase quantities represent material requirements derived from production rather than a complete inventory-based procurement recommendation.

## Future Development

Potential future versions could incorporate:

- inventory and stock coverage;
- supplier allocation;
- lead times and MOQ constraints;
- purchasing price forecasts;
- production seasonality;
- demand forecasting;
- supplier performance KPIs;
- budget vs. actual analysis;
- scenario and sensitivity analysis;
- margin analysis.