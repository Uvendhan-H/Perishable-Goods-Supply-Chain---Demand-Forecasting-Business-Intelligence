# Perishable Goods Supply Chain - Demand Forecasting & Business Intelligence

## Overview
Real-world ML project built on 5+ years of operational data from a banana leaf 
supply chain business supplying Golden Temple, Vellore - a nationally significant 
institutional client.

## Business Problem
Predicting demand, optimizing supply decisions, and analyzing cash flow patterns 
for a perishable goods business with complex seasonality driven by pilgrim 
footfall, Tamil Nadu exam seasons, crop rotation cycles, and weather factors.

## Models Planned
- Time Series Demand Forecasting
- Supply Optimization Classifier
- Cash Flow Prediction

## Tech Stack
Python, Pandas, Scikit-learn, Prophet, Matplotlib, Power BI

## Status
In Progress - EDA Phase Complete. 750 delivery records analysed across 5+ years. Seasonal patterns, weekly supply cycles, and growth trends identified."


## EDA Findings (Phase 1 Complete)

- **Dataset:** 750 delivery days across 1,964 recorded dates (Feb 2021 - Jun 2026)
- **Growth:** 6x increase in average daily supply from 2021 to 2024
- **Seasonality:** Peak supply March-June, trough July-August (monsoon)
- **Weekly pattern:** Thursday/Friday = harvest prep, Saturday/Sunday = primary delivery
- **Supply model:** Demand-driven with unrestricted supply post-2022
- **Key disruptions identified:** COVID waves 2021, college finals 2023, internship period 2025
- **Record month:** March 2026 — 234 bundles (highest in business history)

## Technical Workflow & System Architecture

```text
[Raw 5-Year Excel Ledger] 
          │
          ▼
┌───────────────────────────────────┐
│     1. EXPLORATORY DATA ANALYSIS  │ --> Clean missing data, format dates,
│         (Pandas & NumPy)          │     and handle human accounting errors.
└───────────────────────────────────┘
          │
          ▼
┌───────────────────────────────────┐
│   2. DOMAIN FEATURE ENGINEERING   │ --> Inject custom rules (Exam drops,
│         (Context Injection)       │     Summer velocity, Pilgrim cycles).
└───────────────────────────────────┘
          │
          ▼
┌───────────────────────────────────┐
│    3. PREDICTIVE ML ENGINE        │ --> Train Time-Series, Classifiers,
│        (Scikit-learn / Prophet)   │     and Cash Flow Regressors.
└───────────────────────────────────┘
          │
          ▼
┌───────────────────────────────────┐
│      4. DEPLOYMENT & INTERFACE    │ --> Serve predictions via FastAPI/Dash
│         (FastAPI & Power BI)      │     and display strategic BI metrics.
└───────────────────────────────────┘


