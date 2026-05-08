# 🎧 Spotify Listener Insights & Wrapped Dashboard

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

## 📊 Project Overview

An end-to-end data analytics project analyzing **57,000+ Spotify streaming records** to uncover listening patterns, skip behavior, and user engagement. This project combines Python for data cleaning/analysis with Power BI for interactive visualization.

**Business Problem:** Music streaming services lose millions annually when users skip tracks. Understanding *why* and *when* users skip helps improve recommendations, optimize playlists, and increase user retention.

This project demonstrates:
- Python data cleaning and feature engineering
- Sessionization (creating listening sessions from timestamps)
- Behavioral pattern analysis
- DAX measures for KPIs
- Interactive Power BI dashboard design
- Actionable business recommendations

---

## 📈 Dashboard Preview

### Page 1: Executive Overview
![Executive Overview](outputs/executive_overview.png)
*High-level KPIs, top artists, and listening trends*

### Page 2: Skip Pattern Analysis
![Skip Pattern Analysis](outputs/skip_pattern_analysis.png)
*High-risk artists, hourly skip patterns, and position-based skips*

### Page 3: Listener Behavior
![Listener Behavior](outputs/listener_behavior.png)
*Time of day distribution, session length, and shuffle impact*

### Page 4: Spotify Wrapped
![Spotify Wrapped](outputs/spotify_wrapped.png)
*Personalized listening summary (Top Artist, Total Minutes, Listening Personality)*

---

## 🔍 Key Business Insights

| Insight | Business Impact |
|---------|-----------------|
| **Later tracks skipped 3x more** than first tracks (15% → 47%) | Redesign session continuity features |
| **Diljit Dosanjh** has 62.5% skip rate | Remove from algorithmic playlists |
| **1:00 AM** peak skip rate (21.9%), **9:00 PM** lowest (5.0%) | Schedule releases during optimal hours |
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
| Total Listening Sessions | 7,805 |
| Unique Artists | ~2,500+ |
| Time Period | 2020-2023 |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (Pandas)** | Data cleaning, feature engineering, sessionization |
| **Jupyter Notebook** | Exploratory Data Analysis (EDA) |
| **Power BI Desktop** | Interactive dashboard development |
| **Power Query** | Data loading (minimal - cleaning done in Python) |
| **DAX** | Measures for KPIs and calculations |
| **Matplotlib/Seaborn** | Visualizations in notebook |

---

## 🔧 Python Feature Engineering

Key features created during analysis:

```python
# Sessionization: Group listens with <30 min gaps
df['minutes_since_last'] = df['ts'].diff().dt.total_seconds() / 60
df['new_session'] = (df['minutes_since_last'] > 30) | (df['minutes_since_last'].isna())
df['session_id'] = df['new_session'].cumsum()

# Skip flag generation
df['skipped'] = (df['ms_played'] < 30000).astype(int)

# Time-based features
df['hour'] = df['ts'].dt.hour
df['time_of_day'] = df['hour'].apply(get_time_of_day)
df['is_weekend'] = df['weekday'].isin(['Saturday', 'Sunday'])
