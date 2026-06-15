# PAS Vehicle Hire Invoice Matcher

PAS NW Ltd Vehicle Hire Invoice Reconciliation Tool.

## Purpose

Reconcile vehicle hire invoices against Vehicles.xlsx and allocate costs to jobs/sites.

## Inputs

1. Vehicle Hire Invoice PDF
2. Vehicles.xlsx

## Matching Logic

- Match vehicle registration from invoice
- Match against Column M in Vehicles.xlsx
- Retrieve Job Number / Site
- Retrieve Driver / Assigned User where available

## Outputs

### Annotated PDF
- Original invoice preserved
- Job Number / Site annotated beside each vehicle line
- Blank if no match found

### Excel Summary
- Job Number / Site
- Vehicle Registration
- Driver / Assigned User
- Invoice Line Value
- Vehicle Totals
- Job Totals
- Grand Total

## Dashboard KPIs

- Total Vehicle Lines
- Matched Vehicles
- Unmatched Vehicles
- Match Percentage
- Invoice Total
- Total By Job

## UI

Uses the PAS NW Ltd standard Streamlit UI:
- PAS branding
- KPI cards
- Sidebar
- Animation
- Upload workflow
- Download buttons
