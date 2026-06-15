# PAS Vehicle Hire Invoice Matcher

PAS NW Ltd Vehicle Hire Invoice Reconciliation Tool.

## Purpose

Reconcile vehicle hire invoices against Vehicles.xlsx and allocate costs to jobs/sites.

## Inputs

1. Vehicle Hire Invoice PDF
2. Vehicles.xlsx

## Matching Logic

- Extract vehicle registrations from the invoice PDF
- Match against Vehicle Reg / Registration in Vehicles.xlsx
- Job Number / Site is pulled from Column M in Vehicles.xlsx
- Vehicles on the Off Hire - Sold sheet use the latest Date Returned record
- If no match is found, Job Number / Site remains blank

## Dashboard KPIs

- Total Vehicle Lines
- Matched Vehicles
- Unmatched Vehicles
- Match %
- Invoice Total

## Outputs

### Annotated PDF

- Original invoice layout preserved
- Side-note margin added
- Job Number / Site annotated beside each matched vehicle line
- Blank if no match found

### Excel Report

Tabs included:

1. Vehicle Lines
   - Component No
   - Vehicle Registration
   - Driver / Assigned User
   - Job Number / Site
   - On/Off Hire
   - From
   - To
   - Invoice Line Value
   - VAT
   - Gross
   - Status
   - Grand Total row at the bottom

2. By Job
   - Job Number / Site
   - Total per job
   - Vehicle line count

## UI

Uses the PAS NW Ltd standard Streamlit UI:
- PAS branding
- KPI cards
- Sidebar
- Animation
- Upload workflow
- Download buttons

Version: 1.0.1 Vehicle Hire Simplified
