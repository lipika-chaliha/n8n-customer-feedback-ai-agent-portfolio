# 🐞 Defect Report — Duplicate Google Sheets Record

## Defect Summary

A single customer feedback submission was generating two records in Google Sheets, even though the workflow was expected to create only one consolidated customer record.

## Business Scenario

The customer feedback workflow performs the following activities:

**Customer Feedback → AI Analysis → Personalized Response → Email → Google Sheets**

The workflow intentionally generates two email responses, but the customer information should be stored only once in Google Sheets.

## Expected Result

```text
1 customer submission
        ↓
2 intended emails
        ↓
1 Google Sheets record

## Actual Result

```text
1 customer submission
        ↓
2 intended emails
        ↓
2 Google Sheets records ❌

## Impact

The duplicate record caused the same customer submission to be stored more than once in Google Sheets, affecting data integrity.

## Root Cause Analysis

Multiple workflow items were reaching the Google Sheets node, resulting in duplicate records for the same customer submission.

## Resolution

Instead of modifying the working email logic, I separated the workflow paths and introduced a **Limit** node before Google Sheets.

This ensured that only the intended item reached the Google Sheets storage step.

## Validation After Fix

The workflow was re-executed and validated successfully:

```text
1 customer submission
        ↓
2 intended emails successfully sent
        ↓
1 consolidated Google Sheets record ✅

## Regression Coverage

The duplicate-record scenario was added to regression coverage.

Future validation includes:

- Workflow re-execution
- Branching and workflow logic
- Data mapping changes
- Node configuration changes
- Email path changes
- Google Sheets integration changes
- Duplicate-record prevention
- Data integrity validation

## QA Learning

This defect demonstrated the importance of validating the complete data flow across workflow branches rather than testing individual nodes in isolation.

> **AI automation should be reliable by design, not simply fixed when something breaks.**
