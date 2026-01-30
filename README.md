# 📦 End-to-End Supply Chain Analytics & Automation-N8N-Quadratic-AI-Supabase

An automated data pipeline designed to transform fragmented supply chain data into real-time, actionable business intelligence. This project integrates workflow automation, AI-driven analytics, and cloud-hosted databases to eliminate manual reporting overhead.

---

## 🚀 Project Overview

Supply chain efficiency often breaks down at the data entry level. This project solves that by automating the "Email-to-Insight" pipeline:
* **Automated Ingestion:** No more manual downloads.
* **Centralized Truth:** All data is normalized and stored in a cloud PostgreSQL instance.
* **AI-Enhanced Analysis:** Real-time KPI calculation using natural language and Python-integrated spreadsheets.

## 🛠️ Tech Stack

| Tool | Purpose |
| :--- | :--- |
| **n8n** | Workflow automation & ETL (Extract, Transform, Load) |
| **Supabase** | PostgreSQL Database for persistent data storage |
| **Quadratic AI** | AI-powered spreadsheet for advanced data cleaning & SQL-based analytics |
| **PostgreSQL** | Relational database for merging fact and dimension tables |

---

## 🏗️ System Architecture



1.  **Extraction Layer:** An **n8n** workflow monitors incoming emails, extracts sales data from attachments, and transforms raw formats into structured JSON.
2.  **Database Layer:** Data is ingested into **Supabase (PostgreSQL)**, ensuring scalability and high availability.
3.  **Analytics Layer:** **Quadratic AI** connects directly to Supabase, allowing for:
    * **SQL Blocks** to merge complex tables.
    * **Python Integration** for advanced statistical modeling.
    * **AI Prompts** for rapid data cleaning and insight generation.

---

## 📊 Key Supply Chain KPIs Calculated

The system calculates vital metrics by merging live exchange rates with sales and logistics tables:

* **Line Fill Rate:** Measures the percentage of order lines shipped on the first attempt.
* **OTIF (On-Time In-Full):** Tracks delivery performance against customer deadlines.
* **Currency-Adjusted Reporting:** Leverages live exchange rate APIs to provide accurate financial reporting across different regions.

---

## ⚙️ Workflow Logic

### 1. n8n Automation
* **Trigger:** IMAP/Gmail node watches for specific subject lines.
* **Processing:** Binary data is parsed; JavaScript nodes handle custom schema mapping.
* **Output:** `UPSERT` operations into the Supabase database to avoid duplicate records.

### 2. Quadratic AI Intelligence
* **Live Connection:** Direct connection to the Supabase PostgreSQL port.
* **AI Cleaning:** Used prompt-based logic to handle "dirty" data (e.g., inconsistent date formats or naming conventions).
* **Formulae:** Calculated $OTIF = \frac{Orders\ Shipped\ On\ Time\ and\ In\ Full}{Total\ Orders\ Shipped} \times 100$.

---

## 📈 Future Roadmap

- [ ] Integrate **Slack/Teams notifications** for low inventory alerts.
- [ ] Implement a **Predictive Analytics** model for demand forecasting.
- [ ] Build a front-end **React/Supabase dashboard** for executive summaries.

---

## 👤 Author

**Raghvendra Sharma**
* LinkedIn:[(" https://www.linkedin.com/in/raghvendra-sharma-2a025a308?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app ")]
