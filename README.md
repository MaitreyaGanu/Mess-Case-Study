# 📊 Mess Intelligence Platform

> **Startup-grade DWBI Analytics Suite for Institutional Food Systems**  

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)](https://python.org)
[![Gradio](https://img.shields.io/badge/Gradio-4.20+-FF6B35?logo=gradio)](https://gradio.app)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## ✨ Features

| Module | Description |
|--------|-------------|
| 📈 **Overview** | KPI cards, daily trend with 7-day MA, mess comparison, top-15 vendors |
| 🗑 **Wastage Analysis** | Calendar heatmap + monthly summary (proxy wastage model: `W(d) = E(d)/Ē × 100`) |
| 🔍 **Anomaly Detection** | Z-score statistical outlier flagging with configurable σ threshold |
| 📐 **Benford's Law** | Forensic first-digit χ² goodness-of-fit analysis |
| 🕸 **Network Analysis** | Weighted bipartite mess–vendor graph with Louvain community detection |
| 🔗 **Association Rules** | FP-Growth frequent pattern mining (configurable support/confidence) |
| 📚 **Summary Statistics** | Allows the user to extract meaningful patterns and statistics |

---

## 🚀 Quick Start

https://maitreyaganu.github.io/shodh/
---

## 📂 CSV Format

Your file needs these columns (names are flexible — auto-detected):

| Column | Required | Example |
|--------|----------|---------|
| `date` | ✅ | `2025-08-01` |
| `amount` | ✅ | `150000` |
| `vendor` | Recommended | `Amma Vegetables` |
| `mess` / `unit` | Recommended | `CDH-1` |


---

## 🔬 Methodology

- **Wastage Proxy**: `W(d) = (E(d) / Ē_month) × k` where k = 100 kg baseline constant
- **Benford Test**: χ² goodness-of-fit, df=8, α=0.05 (χ²_critical = 15.51)
- **Network**: Louvain modularity maximization on weighted bipartite graph
- **ARM**: FP-Growth with min_support=0.05, min_confidence=0.60, min_lift=1.0

---

## 📖 Paper Reference

*"Optimizing Institutional Food Systems via Transactional Data: A Residential University Case Study"*  
Maitreya Sameer Ganu (IMS23099) · IISER Thiruvananthapuram · Dec 2025  
Supervisor: Dr. Zakaria Laskar, School of Data Science

---

## 📜 License
MIT License — free to use, modify, deploy.
