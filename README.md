# 📊 ClickHouse Metrics Extractor

Hey! I'm Mohamed Hussain — currently working as an **Associate Data Engineer Intern** 👨‍💻  
This mini-project is my attempt at building a **ClickHouse system metrics extractor** using **Airflow, Docker, and Python**.

If you're curious how to use Airflow to automate metric collection from ClickHouse into CSV files, this might be a helpful reference 🧩

---

## 📁 Project Structure

| Folder | Description |
|--------|-------------|
| `airflow-docker/dags/` | Contains the Airflow DAG that triggers metric extraction every hour |
| `airflow-docker/scripts/` | Python logic to connect to ClickHouse and save system metrics as CSV |
| `airflow-docker/output/` | Output folder where daily CSV files are stored |
| `airflow-docker/docker-compose.yaml` | Docker setup for Airflow and ClickHouse |
| `README.md` | You're reading it! |

---

## 🚀 What This Does

- Connects to a **ClickHouse** instance using `clickhouse-connect`
- Queries the `system.metrics` table for real-time internal metrics
- Uses **Airflow** to schedule the extraction **every hour**
- Saves the output into a **daily CSV file**, appending new rows on each run
- All of this is containerized using **Docker**

---

## 🎯 Why I Did This

- Get comfortable working with **ClickHouse**, a columnar OLAP database
- Practice real-world usage of **Airflow** to automate database jobs
- Learn how to **write structured logs** and **save daily snapshots**
- Build a habit of creating focused, useful micro-projects ⚒️

---

## 🧠 Key Takeaways

- How to use `clickhouse-connect` to query data from ClickHouse
- How to pass execution time to scripts via Airflow context
- How to append logs to a daily CSV in a structured format
- How to containerize and orchestrate this with Docker & Airflow

---

## 🔧 What's Next?

- Store extracted metrics into a **PostgreSQL** or **ClickHouse** table instead of CSV
- Add alerting or visualization (e.g., Grafana) for unusual metric values
- Push CSV files to **cloud storage** (like S3 or GCS)
- Explore extracting metrics from `system.asynchronous_metrics` and `system.events` too

---

## 📸 Proof of Work

(Screenshots of Airflow DAG runs, CSV outputs, or ClickHouse metrics can go here)

---

## 👋 About Me

**Mohamed Hussain S**  
Associate Data Engineer Intern  
[LinkedIn](https://linkedin.com/in/hussainmohhdd) | [GitHub](https://github.com/mohhddhassan)

---

> Learning in public — one cron job at a time ⏱️
