# Patient 360 Analytics Accelerator

## Overview
A comprehensive patient longitudinal view and population health intelligence platform. Provides individual patient 360-degree profiles, population-level analytics, HEDIS quality measure tracking, claims/denial analysis, custom cohort building, and AI-powered clinical recommendations via Snowflake Cortex.

## Features
- **Patient 360 View** — Complete longitudinal profile including demographics, encounters, claims, labs, vitals, medications, care gaps, peer comparison, and AI-powered clinical recommendations
- **Population Overview** — Aggregate metrics, risk distribution, top chronic conditions, comorbidity analysis
- **Care Quality** — HEDIS compliance rates, gap status tracking, benchmark gauges
- **Claims & Denials** — Denial analysis by payer and reason code, financial impact
- **Cohort Builder** — Custom cohort definition with condition, age, gender, risk, and state filters; side-by-side population comparison
- **AI Agent** — Natural language Q&A over your patient population data powered by Snowflake Cortex

## Required Data
This app connects to **your** patient data via table references. You must bind the following tables after installation:

| Reference | Description |
|-----------|-------------|
| DIM_PATIENT | Patient demographics (SCD Type-2 with IS_CURRENT) |
| FACT_ENCOUNTER | Visit/encounter records |
| FACT_CLAIM | Claims with financials |
| FACT_LAB_RESULT | Lab test results |
| FACT_VITAL_SIGN | Vital sign readings |
| FACT_MEDICATION | Prescription fills |
| DIM_DIAGNOSIS | ICD-10 diagnosis reference |
| DIM_PAYER | Insurance/payer reference |
| DIM_PROVIDER | Provider specialty reference |
| MART_QUALITY_MEASURES | HEDIS quality measures |
| MART_COST_UTILISATION | PMPM cost KPIs |

## Setup
1. Install the application from the Marketplace listing
2. Grant the requested privileges
3. Bind each table reference to your corresponding Gold-layer tables
4. Open the Streamlit dashboard

## Version History
- **1.0.0** — Initial marketplace release
