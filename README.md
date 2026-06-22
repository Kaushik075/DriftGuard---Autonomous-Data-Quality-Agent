# DriftGuard---Autonomous-Data-Quality-Agent
Production-style data quality monitoring system built to detect silent failures in telemetry pipelines before they impact dashboards, analytics, and downstream business decisions. 


<img width="1475" height="552" alt="Image" src="https://github.com/user-attachments/assets/cc5ec530-4fbf-42ed-96f6-ef6b24dfa796" />


## Problem

Traditional monitoring tools tell you when a service is down. They don't tell you when your data is wrong.

DriftGuard solves this by detecting:

- Schema Drift
- Null Explosions
- Statistical Outliers (Z-Score Analysis)


## Architecture

n8n → PostgreSQL (Neon) → Detection Engine → Confidence Scoring → SQL Remediation → Slack Alerts

The workflow executes every 6 hours, scans production telemetry data, evaluates anomaly thresholds, logs incidents, and notifies teams with actionable SQL fixes.


## Key Results

- Monitored 250,000+ production telemetry events
- Detected 17% device_os null rate against a 2% baseline
- Generated automated SQL remediation scripts
- Delivered Slack alerts in under 30 seconds
- Achieved 0.92 confidence score for anomaly detection



## Tech Stack

n8n · PostgreSQL · Neon.tech · Python · Slack API · SQL

---



<img width="1181" height="492" alt="Image" src="https://github.com/user-attachments/assets/e3582f7b-f954-427f-8e9f-e66bdc18e0f6" />

---

<img width="1098" height="286" alt="Image" src="https://github.com/user-attachments/assets/5e9514ce-3316-4ba1-b545-d8fa33691af2" />


## Future Improvements

- Scale monitoring to 1M+ events
- Native Python detection engine
- Time-series anomaly detection
- Alert deduplication
- Grafana / Metabase observability dashboard

---

Built by Kaushik Yeddanapudi
