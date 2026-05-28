# ⚽ European Football Player Performance Analytics & Prediction System
### Season 2025/2026 — Top 5 Leagues | Decode Labs Data Science Internship

![Python](https://img.shields.io/badge/Python-3.10-blue) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange) ![sklearn](https://img.shields.io/badge/scikit--learn-ML-green) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 📌 Project Overview

A professional end-to-end football data science project analyzing **2,779 players** across Europe's Top 5 leagues (2025/26 season). The project covers all 5 internship tasks and features **position-specific predictive models** — because a defender is not measured like a forward.

---

## 📁 Project Structure

```
Football-Player-Analytics/
│
├── data/
│   └── players_data-2025_2026.csv        ← 2,779 players × 102 features
│
├── notebooks/
│   └── Football_Analytics_2025_26.ipynb  ← Complete end-to-end notebook
│
├── visuals/                              ← 17 professional charts
│   ├── 01_top_scorers.png
│   ├── 02_league_dashboard.png
│   ├── 03_goals_vs_shots_fwd.png
│   ├── 04_shooting_efficiency_bubble.png
│   ├── 05_age_distribution.png
│   ├── 06_correlation_heatmap.png
│   ├── 07_goals_per90_age_pos.png
│   ├── 08_defender_radar.png
│   ├── 09_goalkeeper_matrix.png
│   ├── 10_midfielder_creativity.png
│   ├── 11_top_nations.png
│   ├── 12_goals_vs_plusminus.png
│   ├── 13_position_donut.png
│   ├── 14_discipline_cards.png
│   ├── 15_minutes_distribution.png
│   ├── 16_feature_importance_all.png
│   └── 17_predicted_vs_actual_all.png
│
├── models/
│   └── position_models.pkl              ← 4 trained position-specific models
│
├── reports/                             ← PDF export destination
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🏆 Key Insights

| Finding | Detail |
|---|---|
| **Peak Age** | 24–27 — highest G+A per 90 mins |
| **Shots on Target → Goals** | Pearson r = 0.91 — strongest predictor |
| **Bundesliga** | Highest avg goals per player |
| **La Liga** | Largest player pool (594 players) |
| **Defenders** | Playing time + fouls best predict defensive output |
| **GK Save%** | GA and SoTA workload dominate prediction |

---

## 🤖 Position-Specific Models

| Position | Target | Best Model | R² |
|---|---|---|---|
| ⚽ Forwards | Goals Scored | Random Forest / Gradient Boosting | >0.95 |
| 🎨 Midfielders | Assists | Random Forest / Gradient Boosting | >0.85 |
| 🛡️ Defenders | Defensive Score | Gradient Boosting | >0.90 |
| 🧤 Goalkeepers | Save Percentage | Ridge / Random Forest | ~0.75 |

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/Football-Player-Analytics.git
cd Football-Player-Analytics

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate       # Mac/Linux
venv\Scripts\activate          # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter
jupyter notebook notebooks/Football_Analytics_2025_26.ipynb
```

---

## 📊 Visualizations Preview

17 charts covering:
- Top scorers & assist leaders
- League comparison dashboard
- Shooting efficiency bubble chart
- Defensive radar profiles (top 5 defenders)
- Goalkeeper performance matrix
- Midfielder creativity map
- Age & position distributions
- Correlation heatmap
- Position-specific feature importance
- Predicted vs actual for all 4 models

---

## 🛠️ Tech Stack

`Python 3.10` · `pandas` · `numpy` · `matplotlib` · `seaborn` · `scikit-learn` · `Jupyter`

---

*Decode Labs Data Science Internship | Season 2025/26*
