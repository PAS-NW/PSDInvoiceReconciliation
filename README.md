# PAS Vehicle Hire Invoice Matcher

PAS NW Ltd Vehicle Hire Invoice Reconciliation Tool.

## Purpose

Reconcile PSD vehicle hire invoices against Vehicles.xlsx and allocate each vehicle line to the correct job/site.

## Inputs

1. Vehicle Hire Invoice PDF
2. Vehicles.xlsx

## Matching Logic

- Match vehicle registration from the invoice against the vehicle registration in Vehicles.xlsx
- Job Number / Site is taken from Column M in Vehicles.xlsx
- For vehicles found on the Off Hire - Sold tab, the latest Date returned row is used
- If no match is found, Job Number / Site is left blank

## Outputs

### Annotated PDF

- Original invoice layout preserved
- Job Number / Site annotated beside each matched vehicle line
- Blank where no match is found

### Excel Report

The Excel report contains:

1. Vehicle Lines
2. By Job

The Vehicle Lines tab includes:

- Component No
- Vehicle Registration
- Driver / Assigned User
- Job Number / Site
- On/Off Hire
- From
- To
- Invoice line value
- VAT
- Gross
- Total per job
- Status
- Grand total at the bottom

## Dashboard KPIs

- Total Vehicle Lines
- Matched Vehicles
- Unmatched Vehicles
- Match %
- Invoice Total

## UI

Uses the PAS NW Ltd standard Streamlit UI:

- PAS branding
- KPI cards
- Sidebar
- Animation
- Upload workflow
- Download buttons
