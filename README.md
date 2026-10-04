# 🚕 Taxi Trip Data — Cleaning & Visualization

A data analysis project exploring NYC taxi trip data: cleaning missing values and visualizing fare, distance, and customer behavior patterns using **Pandas**, **Matplotlib**, and **Seaborn**.

---

## 📌 Project Overview

Taxi services generate large volumes of trip data daily, offering insight into operations, pricing, and rider behavior — but raw data often contains missing values and needs structure before it's useful.

This project acts as an end-to-end mini data-analyst workflow:

- 🧹 **Clean** — detect and handle missing values in the Seaborn `taxis` dataset
- 📊 **Visualize** — build 9 charts spanning basic, statistical, and advanced plot types
- 💡 **Interpret** — summarize patterns in fare, distance, borough activity, and payment behavior

---

## 🗂️ Dataset

**Source:** [`seaborn.load_dataset("taxis")`](https://github.com/mwaskom/seaborn-data) — 6,433 NYC taxi trips, 14 columns (pickup/dropoff timestamps, passengers, distance, fare, tip, tolls, total, payment method, zones & boroughs).

```python
import seaborn as sns
df = sns.load_dataset("taxis")
```

---

## 🧹 Data Cleaning

| Column | Missing | Strategy |
|---|---|---|
| `payment` | 44 | Mode imputation |
| `pickup_zone` | 26 | Mode imputation |
| `dropoff_zone` | 45 | Mode imputation |
| `pickup_borough` | 26 | Mode imputation |
| `dropoff_borough` | 45 | Mode imputation |

All numeric columns (`distance`, `fare`, `tip`, `tolls`, `total`, `passengers`) were already complete — no imputation needed. No duplicate rows were found.

---

## 📈 Visualizations

**Basic (Matplotlib / Pandas Plot)**
- 📉 Line chart — fare over time
- 📊 Bar chart — total fare by pickup borough
- 🥧 Pie chart — trips by payment method
- 📶 Histogram — distribution of trip distance

**Statistical (Seaborn)**
- 📦 Box plot — tip amount by pickup borough
- 🔢 Count plot — number of trips per pickup borough
- ✨ Scatter plot — distance vs. fare, colored by borough

**Advanced (Seaborn)**
- 🔥 Heatmap — correlation between numerical variables
- 🔗 Pair plot — distance, fare, tip, total by pickup zone
- 🎻 Violin plot — fare distribution by payment method

---

## 💡 Key Findings

- 🏙️ **Manhattan dominates** — ~82% of all pickups and the large majority of total fare revenue come from Manhattan.
- 📏 **Fare scales with distance** — distance and fare are strongly correlated (r ≈ 0.9).
- 💳 **Credit card is king** — the large majority of trips are paid by credit card over cash.
- 📐 **Distance is right-skewed** — most trips are short (under ~5 miles), with a long tail of longer rides.
- 💵 **Tipping varies by borough** — boroughs outside Manhattan show more variable, generally lower tips.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data_Wrangling-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Viz-4C8CBF)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📁 Repository Structure

```
├── Data_Visualization.ipynb       # Main notebook: cleaning + all visualizations
├── Taxi_Analysis_Summary.pdf      # One-page findings summary
└── README.md                      # Project overview (this file)
```

---

## ▶️ Getting Started

```bash
# Clone the repo
git clone <your-repo-url>
cd <your-repo-name>

# Install dependencies
pip install pandas matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook Data_Visualization.ipynb
```

---

## 📄 Summary Report

See [`Taxi_Analysis_Summary.pdf`](./Taxi_Analysis_Summary.pdf) for a one-page write-up of the cleaning approach, key findings, and conclusions.

---

## 🙋 Author

Vasumitha —As a part of a Python Data Analytics / Data Visualization assignment.
