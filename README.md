# 🎧 Spotify Listener Behavior Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

## 📊 Project Overview

An interactive Power BI dashboard analyzing **57,000+ Spotify streaming events** to uncover listening patterns, skip behavior, and user engagement. This project demonstrates end-to-end analytics capabilities from raw data to business insights.

**Business Problem:** Music streaming services lose revenue when users skip tracks within the first 30 seconds. Understanding *why* and *when* users skip helps improve recommendations, increase retention, and optimize release timing.

**Key Finding:** Later tracks in a session are skipped **3x more** than first tracks (15% → 47%), suggesting recommendation quality degrades after the first song.

This project demonstrates:
- Python data cleaning and feature engineering
- Sessionization logic (real-world analytics pattern)
- DAX measures for complex calculations
- Interactive dashboard design
- Actionable business recommendations

---

## 📈 Dashboard Preview

### Page 1: Executive Overview
![Executive Overview](/dashboard-preview/screenshots/01-executive-overview.png)
*High-level KPIs, top artists, and listening trends over time*

### Page 2: Skip Pattern Analysis
![Skip Pattern Analysis](/dashboard-previewscreenshots/02-skip-pattern.png)
*High-risk artists, hourly skip patterns, and position-based analysis*

### Page 3: Listener Behavior
![Listener Behavior](/dashboard-previewscreenshots/03-listener-behavior.png)
*Time of day distribution, session length, shuffle impact analysis*

---

## 🔍 Key Business Insights

| Insight | Business Impact |
|---------|-----------------|
| **Later tracks skipped 3x more** than first tracks (15% → 47%) | Improve recommendation algorithms for multi-song sessions |
| **Diljit Dosanjh** has 62.5% skip rate | Remove from algorithmic playlists |
| **1:00 AM** shows peak skip rate (21.9%) | Avoid new releases during late-night hours |
| **9:00 PM** shows lowest skip rate (5.0%) | Optimal time for playlist pushes |
| **Shuffle ON** reduces skips by 2% | Promote shuffle feature more aggressively |
| **18.4%** of sessions are single-track | Add "continue listening" prompts |

---

## 📊 Key Metrics

| Metric | Value |
|--------|-------|
| Total Listens | 57,508 |
| Total Listening Time | ~1,800 hours |
| Overall Skip Rate | 17.8% |
| Average Session Length | 7.2 tracks |
| Total Sessions | 7,805 |
| Unique Artists | 2,500+ |
| Time Period | 2020-2023 |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (Pandas)** | Data cleaning, feature engineering, sessionization |
| **Jupyter Notebook** | Exploratory Data Analysis (EDA) |
| **Power BI Desktop** | Dashboard development, visualization |
| **Power Query** | Data transformation (minor) |
| **DAX** | Measures and calculated columns |
| **Matplotlib/Seaborn** | Notebook visualizations |

---

## 📁 Data Pipeline
