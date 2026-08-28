# Operational Reporting Automation & Performance Dashboard

## Project Overview

This project demonstrates an end-to-end operational reporting workflow using Excel Power Query and Power BI.

The objective was to transform raw operational activity data into a structured, validated, and management-ready reporting solution that highlights schedule performance, overdue work, aging activities, departmental bottlenecks, and data-quality risks.

The project was designed to simulate a realistic operational reporting environment where management needs reliable visibility into:

- Activity completion
- Overdue workload
- Schedule delays
- Aging open activities
- Departmental bottlenecks
- Priority risks
- Data-quality exceptions

---

## Business Problem

Operational teams often rely on manually maintained spreadsheets containing hundreds of activities.

Without structured data validation and automated reporting, management may struggle to answer:

- Which activities are overdue?
- Which departments have the largest backlog?
- Which open activities have been aging the longest?
- Are high-priority activities receiving enough attention?
- Which teams require follow-up?
- Can the underlying reporting data be trusted?

The goal of this project was to create a repeatable reporting workflow that converts raw operational records into actionable management information.

---

## Tools Used

- Microsoft Excel
- Power Query
- Power BI
- DAX
- CSV
- GitHub

---

## Dataset

The project uses a synthetic dataset containing:

- 750 operational activities
- 6 departments
- Activity status and progress
- Planned and actual dates
- Priority classifications
- Approval status
- Responsible teams
- Revision information

The dataset intentionally contains realistic data-quality issues so that the project demonstrates data-cleaning and validation skills rather than using perfectly prepared data.

Examples include:

- Inconsistent category formatting
- Missing priorities
- Missing descriptions
- Duplicate source Activity_ID values
- Invalid actual-date sequences

No confidential employer or client data is used in this project.

---

## Reporting Workflow

```text
Raw CSV
   ↓
Excel Power Query
   ↓
Cleaning & Standardization
   ↓
Data Validation
   ↓
Calculated Operational Fields
   ↓
Clean Analytical Dataset
   ↓
Power BI
   ↓
DAX Measures
   ↓
Management Dashboard
   ↓
Insights & Recommendations