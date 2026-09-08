# Gazpacho Procurement & Raw Material Cost Model

Annual procurement planning and raw material cost model for a fictional gazpacho manufacturer, developed in Microsoft Excel.

The project connects production planning, bill of materials (BOM), purchasing requirements, purchase price variability, raw material costs and operational waste control in a single model.

> **Portfolio project:** all production volumes, recipes, waste assumptions, purchase data and costs used in this model are fictional. The project does not contain confidential or operational data from any real company.

## Business Problem

A food manufacturer needs to translate its monthly production plan into raw material purchasing requirements while controlling:

- ingredient requirements based on the product recipe;
- expected material waste;
- actual quantities purchased;
- multiple purchase prices within the same month;
- raw material spend;
- cost transferred to each litre of finished product;
- expected vs. actual waste;
- monthly and YTD procurement and cost KPIs.

The objective is to create a simple annual model that Procurement and Operations could use to connect production requirements with purchasing and product cost.

## Model Flow

Production Plan  
↓  
Ingredient Master / BOM  
↓  
Net Raw Material Requirement  
↓  
Gross Requirement including Expected Waste  
↓  
Purchasing Plan  
↓  
Weighted Average Purchase Price  
↓  
Raw Material Spend  
↓  
Raw Material Cost per Finished Litre  
↓  
Waste Control & KPIs

## Key Features

- Annual model with monthly production planning.
- Ingredient Master / BOM with recipe percentages and expected waste rates.
- Automatic net and gross raw material requirement calculations.
- Up to two purchase quantities and prices per ingredient and month.
- Weighted average purchase price calculation.
- Required vs. actual purchased quantity control.
- Purchase coverage and purchase variance KPIs.
- Raw material cost transferred to finished product in €/L.
- Manual inputs for manufacturing, packaging and other variable costs.
- Monthly and YTD procurement, production and cost KPIs.
- Expected vs. actual waste monitoring.
- Automatic warning when waste deviation exceeds ±1% of monthly finished production.
- Ingredient cost contribution analysis.

## Core Calculations

### Gross Raw Material Requirement

`Gross Requirement = Net Requirement / (1 - Expected Waste %)`

### Weighted Average Purchase Price

`Weighted Average Price = (Qty1 × Price1 + Qty2 × Price2) / (Qty1 + Qty2)`

### Raw Material Cost per Litre

`Raw Material Cost €/L = Monthly Raw Material Spend / Finished Production L`

### Waste Variance

`Waste Variance = Actual Waste - Expected Waste`

A warning is triggered when the absolute waste variance exceeds 1% of monthly finished production.

## Workbook Structure

| Sheet | Purpose |
|---|---|
| README | Model instructions, scope and methodology |
| Assumptions | Editable business assumptions and control parameters |
| Ingredients_Master | Ingredient master data, BOM and expected waste |
| Production_Plan | Monthly finished-product production inputs |
| Purchasing_Plan | Material requirements, purchases, prices and procurement KPIs |
| Cost_Model | Monthly/YTD costs, waste control and ingredient analysis |

## Example Scenario

The template contains an illustrative January production plan of **100,000 litres**.

Based on the fictional recipe and expected waste assumptions, this generates approximately:

- **100,000 kg** net raw material requirement;
- **109,651 kg** gross raw material requirement;
- **9,651 kg** expected raw material waste.

Purchase prices remain blank so the workbook can be used as an operational template.

## Scope & Limitations

Version 1 intentionally excludes:

- demand and sales forecasting;
- seasonality;
- inventory management;
- supplier lead times;
- minimum order quantities (MOQ);
- safety stock;
- logistics costs;
- fixed manufacturing overhead;
- selling price and margin.

These areas could be incorporated in future versions of the model.

## Repository Structure

```text
gazpacho-procurement-cost-model/
├── README.md
├── docs/
│   └── model_logic.md
├── model/
│   ├── EN/
│   └── ES/
└── screenshots/

## Tools & Skills Demonstrated

### Microsoft Excel

- Structured data modelling
- Formulas and linked calculations
- Input/calculation separation
- Weighted average calculations
- Conditional controls and alerts
- Monthly and YTD KPI design
- Business-oriented reporting

### Procurement & Operations

- BOM-based purchasing requirements
- Raw material planning
- Purchase price analysis
- Weighted average purchase price
- Required vs. actual purchase tracking
- Purchase coverage and variance analysis
- Raw material cost contribution
- Waste and yield monitoring
- Finished-product cost analysis

### Git & GitHub

- Repository structure
- Version control
- Incremental commits
- Project documentation
- File organisation
- Portfolio publishing

## Language Versions

The model is available in:

- **English** — primary portfolio version
- **Spanish** — equivalent localized version

Both workbooks use the same business logic, calculations, assumptions and control methodology.

## Author

**Nieves Martí**

Procurement | Sourcing | Supply Chain | Business Intelligence