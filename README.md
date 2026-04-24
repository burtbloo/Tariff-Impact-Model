# Tariff Impact Model

An Excel-based scenario model that quantifies how import tariffs by country of origin affect landed cost, target selling price, and gross margin across a produce wholesale catalog.

## Overview

This workbook was originally built during a financial analyst internship to model tariff exposure across an import-heavy catalog. It's been rebuilt here as a portfolio piece with fully synthetic data — no proprietary supplier, pricing, or margin information is included.

The model covers 230+ SKUs across 21 countries of origin and 10 product categories, with scenario-driven tariff rates that flow through to per-SKU landed cost and margin calculations.

## What's in the workbook

- **Dashboard** — summary KPIs and a country-level view of SKU counts, average base costs, tariff scenarios, and total cost impact
- **Tariff Rates** — editable tariff rates by country (Baseline, Scenario 1, Scenario 2)
- **Product Catalog** — master SKU list with origin, category, base cost, and target markup
- **Impact Analysis** — per-SKU landed cost, margin, and scenario deltas with conditional formatting on margin erosion
- **Methodology** — documented assumptions, definitions, and model limitations

## How the model works

Landed cost is calculated as `(Base Cost + Freight) × (1 + Tariff Rate)`. Target selling price is fixed at the baseline scenario (price-locked), so tariff increases compress margin rather than flow to the customer. This isolates the pure margin impact of tariff changes.

The Impact Analysis tab flows through all calculations automatically — changing any blue input cell (tariff rate, markup, origin, base cost) recalculates the entire model.

## Stack

- Microsoft Excel (openpyxl-compatible)
- ~3,200 formulas across 5 sheets
- Conditional formatting and cross-sheet lookups (VLOOKUP, SUMPRODUCT, AVERAGEIF)

## Limitations

This is a simplified model. It does not account for seasonality, spoilage, FX risk, weight- or volume-based freight, or price elasticity. These would be separate builds in a full landed-cost analysis.

## About

Built by Kurt Lu. Connect on [LinkedIn](https://linkedin.com/in/kurtlu10/).
