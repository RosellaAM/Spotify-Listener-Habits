# 🎧 Spotify Listener Behavior Analysis

## Project Overview

This project analyzes Spotify streaming history to uncover listening patterns, skip behavior, and user engagement. Built as a portfolio piece for a **Junior Data Analyst/Scientist** role.

**Business Problem:** Music streaming services lose revenue when users skip tracks. Understanding *why* and *when* users skip helps improve recommendations and retention.

**Key Insight:** Later tracks in a session are skipped **3x more** than first tracks (15% → 47%).

## Tools Used

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data cleaning, feature engineering, sessionization |
| Jupyter Notebook | Exploratory Data Analysis (EDA) |
| Power BI | Interactive dashboard |
| Matplotlib/Seaborn | Visualizations |

## Data Source

[160k Spotify Streaming History](https://www.kaggle.com/datasets/adhok93/160k-spotify-streaming-history) from Kaggle

## Key Findings

| Finding | Insight |
|---------|---------|
| **Top skip artist** | Diljit Dosanjh - 62.5% skip rate |
| **Worst hour** | 1:00 AM (21.9% skip rate) |
| **Best hour** | 9:00 PM (5.0% skip rate) |
| **Shuffle impact** | Shuffle ON reduces skips by 2% |
| **Session length** | Average 7.2 tracks per session |
| **Single-track sessions** | 18.4% of all sessions |

## Repository Structure
