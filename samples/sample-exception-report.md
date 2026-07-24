# PrevailAudit Sample Exception Report

Date: 2026-07-24

This is a synthetic demonstration report. It is not legal advice, payroll advice, or a compliance guarantee.

## Customer

- Company: Sample Contractor LLC
- Project: Sample Forest Bridge Repair
- Award ID: SAMPLE-127EAX26P0007
- Agency: Sample Forest Service District
- Payroll week ending: 2026-07-17
- Files reviewed:
  - `sample-payroll-export-week-ending-2026-07-17.csv`
  - `sample-wh347-extract-week-ending-2026-07-17.csv`
  - `sample-wage-determination-table.csv`
  - `sample-daily-log-week-ending-2026-07-17.csv`

## Executive Summary

PrevailAudit found 5 critical findings, 4 review-needed findings, and 1 missing-data pattern in the sample packet.

Most important items before submission:

- W001 appears below the required Laborer base wage and fringe values in the sample wage table.
- W003 appears below the required Carpenter fringe value.
- W006 appears in payroll and daily logs but is missing from the WH-347 extract.
- W007 appears in the WH-347 extract but is missing from the payroll export.
- W004's WH-347 packet row is marked as missing statement-of-compliance and signature indicators.

## Critical Findings

| Severity | Worker/Packet | Issue | Evidence | Recommended Next Step |
| --- | --- | --- | --- | --- |
| Critical | W001 Alex Rivera | Base wage below sample Laborer requirement | Payroll base rate `27.90`; wage table requires `28.40` | Review payroll rate and correct before submission. |
| Critical | W001 Alex Rivera | Fringe below sample Laborer requirement | Payroll fringe cash `10.00`; wage table requires `14.25`; no benefit credit supplied | Add documented fringe credit or correct cash fringe. |
| Critical | W003 Sam Patel | Fringe below sample Carpenter requirement | Payroll fringe cash `15.00`; wage table requires `17.10`; no benefit credit supplied | Confirm fringe benefit credit or correct reported fringe. |
| Critical | W006 Casey Nguyen | Worker present in payroll export and daily log but missing from WH-347 extract | Payroll shows 20 hours; daily log shows five 4-hour days; no WH-347 row found | Add worker row or confirm why worker is excluded. |
| Critical | W007 Riley Stone | Worker present in WH-347 extract but missing from payroll export | WH-347 shows 8 hours and gross wages; no payroll row found | Reconcile source payroll export or remove incorrect WH-347 row. |

## Review-Needed Findings

| Severity | Worker/Packet | Issue | Evidence | Recommended Next Step |
| --- | --- | --- | --- | --- |
| Review | W003 Sam Patel | Classification label differs between payroll and WH-347 | Payroll says `Carpenter`; WH-347 says `Carpenter / Finish` | Confirm mapping to the wage determination class. |
| Review | W001 Alex Rivera | Overtime-sensitive row needs review | Payroll shows 40 regular hours and 4 overtime hours | Confirm overtime calculation and supporting daily/timecard detail. |
| Review | W004 Taylor Brooks | Classification label differs from wage table | Payroll says `Operator`; WH-347 says `Operating Engineer`; wage table uses `Operating Engineer` | Normalize class label before submission. |
| Review | W004 Taylor Brooks | Overtime-sensitive hours need review | Payroll shows 46 regular hours and 0 overtime hours; daily log has two 10-hour days | Confirm overtime treatment and source system configuration. |

## Missing Data

| Missing Item | Why It Matters | Suggested Source |
| --- | --- | --- |
| Benefit-credit detail | Fringe pass/fail cannot be proven if benefits are paid outside cash fringe fields | Payroll benefit report or fringe allocation worksheet |

## Payroll-To-WH-347 Reconciliation

| Check | Result | Notes |
| --- | --- | --- |
| Worker list matches | Fail | W006 missing from WH-347; W007 missing from payroll export. |
| Week-ending date matches | Pass | All rows use 2026-07-17. |
| Classifications match | Review | W003 and W004 labels differ across sources. |
| Hours match | Pass with review | Matched rows reconcile total hours, but W004 overtime treatment needs review. |
| Gross wages match | Pass for matched workers | Matched rows reconcile gross wages. |
| Deductions/net wages match | Pass for matched workers | Matched rows reconcile deductions and net wages. |
| Statement of compliance present | Fail | W004 row is marked false/missing in the WH-347 extract. |

## Wage Determination Review

| Worker/Class | Source Classification | Wage Determination Match | Base Wage Check | Fringe Check | Notes |
| --- | --- | --- | --- | --- | --- |
| W001 Alex Rivera | Laborer | Exact match | Fail | Fail | Base and fringe shortfalls in sample data. |
| W002 Morgan Lee | Electrician | Exact match | Pass | Pass | No issue found in sample data. |
| W003 Sam Patel | Carpenter / Finish | Close match | Pass | Fail | Classification mapping and fringe need review. |
| W004 Taylor Brooks | Operator / Operating Engineer | Close match | Pass | Pass | Overtime-sensitive row. |
| W005 Jordan Kim | Truck Driver | Exact match | Pass | Pass | No issue found in sample data. |
| W006 Casey Nguyen | Laborer | Exact match | Pass | Pass | Missing from WH-347 extract. |
| W007 Riley Stone | Laborer | Exact match | Missing payroll source | Missing payroll source | Present only in WH-347 extract. |

## Overtime-Sensitive Rows

| Worker | Week Ending | Hours Signal | Reason For Review |
| --- | --- | --- | --- |
| W001 Alex Rivera | 2026-07-17 | 40 regular hours and 4 overtime hours | Confirm overtime calculation and packet presentation. |
| W004 Taylor Brooks | 2026-07-17 | 46 regular hours and 0 overtime hours | Confirm whether overtime should have been separated. |

## Recommended Correction Workflow

1. Correct W001 base wage and fringe records or document benefit credits.
2. Confirm W003 class mapping and fringe credit.
3. Reconcile W006 and W007 across payroll export and WH-347 packet.
4. Confirm W004 overtime treatment and statement-of-compliance signature status.
5. Re-export the certified payroll packet.
6. Run a second review before submission.

## Product Feedback Prompt

If this were your packet:

- Which finding would save the most rework?
- Which finding is obvious or low-value?
- Would this report be useful every payroll week?
- Would you pay $149/month to run this before submission?

## Disclaimer

PrevailAudit provides document review and workflow support. This report is not legal advice and does not guarantee compliance with the Davis-Bacon and Related Acts, the Copeland Act, the Contract Work Hours and Safety Standards Act, or any contract-specific requirement.
