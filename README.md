# 🚀 Objectif du projet
Prototyper un **“Datamart Santé & Prévoyance”** pour Crédit Agricole Assurances, couvrant :

- **Data préparation & datamarts** sous SAS et Python/SQL  
- **Visualisation & reporting** avec Power BI et automatisation  
- **Analyses descriptives, exploratoires et prédictives** sur tarification et rentabilité  
- **Documentation & bonnes pratiques** (Excel/VBA, Git, modularité)  

Vous montrerez votre maîtrise end-to-end : ingestion de sources diverses, pipelines ETL, construction de datamarts, dashboards interactifs, reporting automatisé et modélisation prédictive simple.

---

## 📅 Planning détaillé sur 5 jours ouvrés (+ 2 jours de buffer)

| Jour   | Tâches clés                                                                                                                                                                                                                                                              |
|:------:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Jour 1** | **Init projet & collecte**<br>• `git init` + `.gitignore` + venv Python<br>• Fichiers SAS de sample clients et contrats (simulés) + CSV historiques sinistres<br>• Conception du modèle conceptuel de datamart (star schema) |
| **Jour 2** | **ETL & datamart**<br>• Scripts SAS pour extraction, nettoyage et harmonisation (formats, doublons, dates)<br>• Python/SQL pour alimenter un datalake local (SQLite ou Postgres portable) et construire le datamart en tables fact et dimensions |
| **Jour 3** | **Reporting & dashboards**<br>• Prototype Power BI : tableaux de bord tarification vs rentabilité par segment<br>• Automatisation Excel/VBA : génération quotidienne de comptes de résultat et exports CSV pour BI |
| **Jour 4** | **Analyse exploratoire & descriptif**<br>• Jupyter Notebook : distribution prime, taux de sinistralité, corrélations variables clés<br>• Scripts Python pour calculer KPIs (loss ratio, NPS estimé, churn rate) et export vers datamart |
| **Jour 5** | **Modélisation prédictive**<br>• Modèle de scoring sinistres (Logistic Regression / Random Forest) en Python avec scikit-learn<br>• Évaluation (AUC, confusion matrix) et intégration des scores dans le datamart |
| **Jour 6** | **Automatisation & documentation**<br>• Orchestration ETL + scoring via Airflow léger (ou scripts batch)<br>• Rédaction `README.md` : architecture, installation SAS/Python, usage Power BI, maintenance datamart |
| **Jour 7** | **Tests & packaging**<br>• Tests unitaires Python (pytest) et validation SAS (macros de contrôle)<br>• Finalisation `requirements.txt`, schémas ER dans `docs/`, commit & push sur GitHub<br>• Buffer pour itérations et polish |

---

## ⚙️ Structure Git finale

```bash
caisse-assurances-datamart/
├── data/
│   ├── raw/                     # SAS datasets et CSV historiques
│   └── processed/               # fichiers cleansed
├── docs/
│   └── datamart_schema.png      # diagramme star schema
├── src/
│   ├── etl/
│   │   ├── extract.sas          # extraction & nettoyage SAS
│   │   ├── transform.sas        # harmonisation & datamart SAS
│   │   └── load_sql.py          # chargement datalake → datamart SQL
│   ├── reporting/
│   │   ├── generate_excel.vba   # macro VBA rapports
│   │   └── powerbi_template.pbix# dashboard Power BI connecté au datamart
│   ├── analysis/
│   │   └── eda.ipynb            # exploratoire & calcul KPIs
│   ├── modeling/
│   │   └── sinistre_model.py    # scoring sinistres, evaluation
│   └── orchestrator.py          # lancement batch ETL + scoring
├── tests/
│   ├── test_etl_sas.py
│   ├── test_load_sql.py
│   ├── test_model.py
│   └── test_reporting.py
├── docs/
│   └── datamart_schema.png
├── .gitignore
├── README.md
└── requirements.txt
