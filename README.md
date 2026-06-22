# DriftGuard---Autonomous-Data-Quality-Agent
Production-style data quality monitoring system built to detect silent failures in telemetry pipelines before they impact dashboards, analytics, and downstream business decisions. 


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

## Screenshots




## Future Improvements

- Scale monitoring to 1M+ events
- Native Python detection engine
- Time-series anomaly detection
- Alert deduplication
- Grafana / Metabase observability dashboard

---

Built by Kaushik Yeddanapudi
