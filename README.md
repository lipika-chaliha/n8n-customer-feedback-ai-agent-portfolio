# 🤖 Customer Feedback Sentiment AI Agent

An AI-powered customer feedback automation workflow built using **n8n, AI, Gmail and Google Sheets**, with a strong focus on **Quality Engineering, data integrity and workflow reliability**.

## ⭐ Portfolio Highlights

This project demonstrates my practical experience in combining **AI Automation + Quality Engineering + Software Testing**.

- 🤖 **n8n AI Workflow Automation**
- 🧠 **AI/LLM-based sentiment and response generation**
- 🧪 **End-to-end Quality Engineering**
- 🔍 **Data flow and data mapping validation**
- 🐞 **Real defect identification and root-cause analysis**
- 🔧 **Defect resolution using workflow logic**
- 🔄 **Regression testing and re-execution**
- 📊 **Data integrity and duplicate-record validation**
- 📧 **Gmail integration testing**
- 📋 **Google Sheets integration and validation**

## 🧪 What I Tested

The workflow was validated from an end-to-end Quality Engineering perspective.

Key testing areas included:

- Functional testing
- End-to-end workflow validation
- Branching and workflow logic
- AI output validation
- Data mapping validation
- Email delivery validation
- Duplicate processing
- Data integrity
- Edge-case scenarios
- Regression testing
- Workflow re-execution

## 🐞 Defect Investigation

During testing, I identified a duplicate-record issue where:

**1 customer submission → 2 intended emails → 2 Google Sheets records**

The expected behavior was:

**1 customer submission → 2 intended emails → 1 Google Sheets record**

I analyzed the workflow data flow and identified that multiple workflow items were reaching the Google Sheets step.

Instead of changing the working email logic, I separated the workflow paths and introduced a **Limit** node before Google Sheets.

### Result

**1 customer submission → 2 intended emails → 1 consolidated Google Sheets record**

The scenario was subsequently added to regression coverage.


## 🎯 Project Overview

This project automates the customer feedback process from submission to AI analysis, personalized response generation, email communication and data storage.

The project demonstrates how **AI Automation + Quality Engineering** can be combined to build workflows that are not only functional, but also **reliable, testable and maintainable**.

## 🔄 Workflow

**Customer Feedback → AI Analysis → Sentiment & Points → Personalized Response → Email → Google Sheets**

### How the Workflow Works

1. Customer submits feedback through a form.
2. n8n receives the feedback submission.
3. AI analyzes the customer feedback.
4. Sentiment and points are determined.
5. AI generates a personalized response.
6. Two intended email responses are generated and sent.
7. Customer information and AI-generated results are stored in Google Sheets.

## 🛠️ Technologies Used

- **n8n** — Workflow automation
- **AI / LLM** — Sentiment analysis and response generation
- **Gmail** — Automated email communication
- **Google Sheets** — Customer data storage
- **Quality Engineering** — Workflow validation and reliability testing

## 🧪 QA & Testing Approach

The workflow was tested from an end-to-end Quality Engineering perspective.

Testing areas included:

- Functional testing
- End-to-end workflow validation
- Branching and workflow logic
- AI output validation
- Data mapping validation
- Email delivery validation
- Duplicate processing
- Data integrity
- Edge-case scenarios
- Regression testing
- Workflow re-execution

## 🐞 Defect Identified

During testing, I discovered that a single customer feedback submission was generating **two records in Google Sheets**.

### Expected Result

**1 customer submission → 2 intended emails → 1 Google Sheets record**

### Actual Result

**1 customer submission → 2 intended emails → 2 Google Sheets records ❌**

The email functionality was working correctly. The defect was caused by multiple workflow items reaching the Google Sheets step, resulting in duplicate records.

## 🔧 Resolution

Instead of modifying the working email logic, I separated the workflow paths and introduced a **Limit node before Google Sheets**.

This ensured that only the intended item reached the Google Sheets storage step.

## ✅ Final Result

The workflow was validated to ensure the intended business flow:

**1 customer submission**

↓

**2 intended emails successfully sent**

↓

**1 consolidated Google Sheets record**

The duplicate-record scenario was also added to the regression coverage so it can be revalidated whenever relevant workflow nodes, mappings or logic are changed.

## 💡 Quality Engineering Learning

This project reinforced an important principle:

> **AI automation should be reliable by design, not simply fixed when something breaks.**

Building an AI workflow is only the beginning. Validating data flow, branches, integrations, AI outputs, edge cases and regression scenarios is equally important for production reliability.

## 📸 Workflow Overview

![n8n Customer Feedback AI Agent Workflow](screenshots/workflow-overview.png)

The workflow connects customer feedback submission, AI analysis, personalized response generation, email communication and Google Sheets storage.

## 🔐 Security

This repository contains a **sanitized portfolio version** of the n8n workflow.

No production API keys, passwords, access tokens, private credentials or confidential customer information should be included.

Environment-specific identifiers and credential references have been replaced with placeholders.

The workflow is presented using test/sample data for demonstration purposes.

## 👩‍💻 Author

**Lipika Chaliha**

AI-Driven QA Test Lead | 11+ Years QA Experience | AI Testing | Quality Engineering | n8n Workflow Automation | ISTQB Certified
