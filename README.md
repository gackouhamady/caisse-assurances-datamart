# 🚀 Project Objective

Prototype a **“Health & Insurance Datamart”** for Crédit Agricole Assurances, covering:

* **Data preparation & datamarts** in SAS and Python/SQL
* **Visualization & reporting** with Power BI and automation
* **Descriptive, exploratory & predictive analyses** on pricing and profitability
* **Documentation & best practices** (Excel/VBA, Git, modularity)

You will demonstrate end-to-end mastery: ingestion of diverse sources, ETL pipelines, datamart construction, interactive dashboards, automated reporting, and simple predictive modeling.

---

## 📅 Detailed 5-day working plan (+ 2 days buffer)

|                                                             Day                                                             | Key tasks                              |
| :-------------------------------------------------------------------------------------------------------------------------: | :------------------------------------- |
|                                                          **Day 1**                                                          | **Project init & gathering**           |
|                                          • `git init` + `.gitignore` + Python venv                                          |                                        |
|                       • Sample SAS files for clients and contracts (simulated) + historical claims CSV                      |                                        |
|                                       • Conceptual datamart model design (star schema)                                      |                                        |
|                                                          **Day 2**                                                          | **ETL & datamart**                     |
|                    • SAS scripts for extraction, cleaning, and harmonization (formats, duplicates, dates)                   |                                        |
| • Python/SQL to populate a local datalake (SQLite or portable Postgres) and build the datamart as fact and dimension tables |                                        |
|                                                          **Day 3**                                                          | **Reporting & dashboards**             |
|                            • Power BI prototype: pricing vs. profitability dashboards by segment                            |                                        |
|                             • Excel/VBA automation: daily P\&L generation and CSV exports for BI                            |                                        |
|                                                          **Day 4**                                                          | **Exploratory & descriptive analysis** |
|                     • Jupyter Notebook: premium distribution, loss ratio, correlations of key variables                     |                                        |
|             • Python scripts to compute KPIs (loss ratio, estimated NPS, churn rate) and export to the datamart             |                                        |
|                                                          **Day 5**                                                          | **Predictive modeling**                |
|                   • Claims scoring model (Logistic Regression / Random Forest) in Python with scikit-learn                  |                                        |
|                       • Evaluation (AUC, confusion matrix) and integration of scores into the datamart                      |                                        |
|                                                          **Day 6**                                                          | **Automation & documentation**         |
|                            • Orchestrate ETL + scoring via lightweight Airflow (or batch scripts)                           |                                        |
|                  • Write `README.md`: architecture, SAS/Python setup, Power BI usage, datamart maintenance                  |                                        |
|                                                          **Day 7**                                                          | **Testing & packaging**                |
|                               • Python unit tests (pytest) and SAS validation (control macros)                              |                                        |
|                        • Finalize `requirements.txt`, ER schemas in `docs/`, commit & push to GitHub                        |                                        |
|                                            • Buffer for iterations and polishing                                            |                                        |

---

## ⚙️ Final Git Structure

```bash
caisse-assurances-datamart/
├── data/
│   ├── raw/                     # SAS datasets and historical CSVs
│   └── processed/               # cleansed files
├── docs/
│   └── datamart_schema.png      # star schema diagram
├── src/
│   ├── etl/
│   │   ├── extract.sas          # SAS extraction & cleaning
│   │   ├── transform.sas        # SAS harmonization & datamart
│   │   └── load_sql.py          # datalake → SQL datamart loading
│   ├── reporting/
│   │   ├── generate_excel.vba   # VBA reporting macro
│   │   └── powerbi_template.pbix# Power BI dashboard connected to datamart
│   ├── analysis/
│   │   └── eda.ipynb            # exploratory analysis & KPI computation
│   ├── modeling/
│   │   └── claims_model.py      # claims scoring & evaluation
│   └── orchestrator.py          # batch ETL + scoring launcher
├── tests/
│   ├── test_etl_sas.py
│   ├── test_load_sql.py
│   ├── test_model.py
│   └── test_reporting.py
├── .gitignore
├── README.md
└── requirements.txt
```
