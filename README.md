# Building an Automated MEAL Data Pipeline: KoboToolbox to Power BI

![Pipeline Architecture](https://img.shields.io/badge/Pipeline-KoboToolbox%20%E2%86%92%20PowerQuery%20%E2%86%92%20Python%20%E2%86%92%20PowerBI-blue)
![Language](https://img.shields.io/badge/Language-M%20%7C%20Python%203.x-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

Welcome to the official repository for the **"From KoboToolbox to Power BI: Building an Automated MEAL Data Pipeline"** workshop. This repository contains all code snippets, template queries, Python quality assurance scripts, and bilingual documentation needed to transition from manual CSV exports to a zero-touch, automated data pipeline.

---

## 📌 Overview

Manual CSV downloads, broken formulas, unlinked survey repeat groups, and schema shifts slow down Monitoring, Evaluation, Accountability, and Learning (MEAL) teams and introduce reporting errors. 

This repository provides an end-to-end framework to:
1. **Connect** KoboToolbox directly to Power BI via REST API using parameterized authentication (no hardcoded tokens).
2. **Handle Schema Drift** dynamically so XLSForm changes (added/removed questions) don't crash reports.
3. **Model Relational Data** by linking main survey forms to nested repeat groups using `_index` and `_parent_index`.
4. **Automate Quality Assurance** using embedded Python (`pandas`) to flag missing fields, invalid date logic, and statistical outliers upon refresh.

---

## 📂 Repository Structure

```text
.
├── README.md                           # Repository documentation (English)
├── README_FR.md                        # Bilingual documentation (Français)
├── docs/
│   ├── Step_By_Step_Guide_EN.pdf       # Full implementation guide (English)
│   ├── Step_By_Step_Guide_FR.pdf       # Guide d'implémentation (Français)
│   └── UI_Terminology_Mapping.md      # English-to-French Power BI UI reference
├── m_code/
│   ├── 01_kobo_api_ingestion.m         # Schema-resilient Kobo API connection
│   └── 02_repeat_group_linking.m       # Parent-child relational transformation
├── python/
│   └── qa_checks.py                    # Pandas script for automated QA flags
└── templates/
    ├── sample_kobo_form.xlsx           # Demo XLSForm structure
    └── pipeline_template.pbix          # Pre-configured Power BI Desktop template
