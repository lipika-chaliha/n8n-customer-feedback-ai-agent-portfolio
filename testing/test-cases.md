# 🧪 QA Test Cases — Customer Feedback Sentiment AI Agent

## Test Objective

Validate the end-to-end customer feedback workflow, including form submission, AI analysis, sentiment generation, personalized response generation, email delivery, Google Sheets storage, data integrity and duplicate prevention.

## Test Cases

| TC ID | Test Scenario | Expected Result | Status |
|---|---|---|---|
| TC-001 | Submit valid customer feedback | Feedback is accepted and workflow starts successfully | Pass |
| TC-002 | Verify AI analyzes feedback | AI generates the expected analysis | Pass |
| TC-003 | Verify sentiment generation | Sentiment value is generated correctly | Pass |
| TC-004 | Verify personalized response | AI generates a customer-specific response | Pass |
| TC-005 | Verify email generation | Intended email responses are generated successfully | Pass |
| TC-006 | Verify email delivery | Emails are successfully sent through Gmail | Pass |
| TC-007 | Verify Google Sheets storage | Customer information is stored correctly | Pass |
| TC-008 | Verify data mapping | Customer name, feedback and AI output are mapped correctly | Pass |
| TC-009 | Verify duplicate record prevention | Only one consolidated Google Sheets record is created | Pass |
| TC-010 | Re-run the workflow | Workflow behaves consistently without unintended duplicate records | Pass |
| TC-011 | Validate empty feedback | Workflow handles missing feedback appropriately | To Validate |
| TC-012 | Validate special characters | Workflow processes special characters without data corruption | To Validate |
| TC-013 | Validate long feedback | Workflow handles lengthy customer feedback appropriately | To Validate |
| TC-014 | Validate AI output fields | Required AI response fields are populated | To Validate |
| TC-015 | Regression after workflow changes | Existing functionality continues to work after node or mapping changes | To Validate |

## Key Regression Scenario

### Scenario

Validate the complete customer feedback flow:

**1 customer submission → 2 intended emails → 1 Google Sheets record**

### Validation Points

- Correct workflow execution
- Correct AI analysis
- Correct sentiment
- Correct customer data mapping
- Two intended email responses
- One consolidated Google Sheets record
- No duplicate records
- No unintended data loss

## QA Focus

The primary QA focus is **data flow integrity across multiple workflow branches and integrations**.

The workflow should remain reliable when relevant nodes, mappings or business logic are modified.
