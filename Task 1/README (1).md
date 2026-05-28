# ⚽ European Football Analytics — 2025/26 Season

> **Data Science Internship Project | Decode Labs | 2025–2026**

A complete end-to-end data science project analyzing player statistics from the top 5 European football leagues in the 2025–2026 season. Built across all 5 internship tasks — from raw data loading to a machine learning role classifier and custom performance scoring system.

---

## 📌 Project Overview

| Task | Description | Status |
|------|-------------|--------|
| 1 — Data Collection & Understanding | Load dataset, explore structure, document all 53 columns | ✅ Complete |
| 2 — Data Cleaning & Preprocessing | Remove duplicates, standardize positions, fill missing values | ✅ Complete |
| 3 — Exploratory Data Analysis | Goals, shooting, defending, age, and GK insights | ✅ Complete |
| 4 — Data Visualization | 10 professional charts using matplotlib and seaborn | ✅ Complete |
| 5 — Predictive Model | Random Forest role classifier + position-aware Performance Score | ✅ Complete |

---

## 📂 Repository Structure

```
Football-Analytics-DecodeLabs/
│
├── data/
│   └── players_data_light-2025_2026.csv   # Main dataset (2,779 players, 53 columns)
│
├── notebooks/
│   └── football_analytics_final.ipynb     # Complete project — all 5 tasks in one notebook
│
├── visuals/
│   ├── 01_top_scorers.png
│   ├── 02_top_assists.png
│   ├── 03_goals_by_league.png
│   ├── 04_position_distribution.png
│   ├── 05_age_distribution.png
│   ├── 06_goals_vs_assists.png
│   ├── 07_correlation_heatmap.png
│   ├── 08_stats_by_position.png
│   ├── 09_top_defenders.png
│   ├── 10_top_goalkeepers.png
│   ├── 11_confusion_matrix.png
│   ├── 12_feature_importance.png
│   └── 13_performance_scores.png
│
├── models/
│   ├── role_classifier.pkl                # Trained Random Forest model
│   ├── scaler.pkl                         # StandardScaler used during training
│   └── label_encoder.pkl                  # LabelEncoder for position labels
│
├── docs/
│   └── Football_Analytics_Explanation_FINAL.docx  # Full line-by-line code explanation
│
├── README.md                              # This file
└── requirements.txt                       # Python dependencies
```

---

## 📊 Dataset

**Name:** European Football Players Statistics 2025–2026  
**Source:** FBref (Football Reference)  
**File:** `players_data_light-2025_2026.csv`

| Property | Value |
|----------|-------|
| Players (rows) | 2,779 |
| Features (columns) | 53 |
| Leagues | Premier League, La Liga, Bundesliga, Serie A, Ligue 1 |
| Season | 2025–2026 |

**Column categories:**
- **Identity:** Player, Nation, Position, Squad, League, Age
- **Playing Time:** Matches Played, Starts, Minutes, 90s
- **Attacking:** Goals, Assists, G+A, Penalties
- **Shooting:** Shots, Shots on Target, SoT%, G/Sh, G/SoT
- **Defending:** Tackles Won, Interceptions, Crosses
- **Goalkeeping:** GA, Saves, Save%, Clean Sheets, W/D/L

---

## 🔍 Key Findings

- **Harry Kane** leads all scorers with **33 goals** in the Bundesliga
- **Goal-scoring is rare** — median goals per player = 0, only ~8% of players reach double figures
- **Prime age zone** confirmed at **23–29 years** for peak goal contributions
- **Goalkeeper stats** (Saves, GA, Save%, CS) are the strongest position identifiers for the ML model
- **Defensive midfielders** are the hardest position to classify — their stats overlap significantly with central defenders
- **Top Save%** keepers consistently save 75–80% of shots on target

---

## 🤖 Machine Learning Model

**Algorithm:** Random Forest Classifier  
**Task:** Predict player position (FW / MF / DF / GK) from statistics alone

| Setting | Value |
|---------|-------|
| Trees (n_estimators) | 200 |
| Max depth | 12 |
| Features used | 14 |
| Train / Test split | 80% / 20% |
| Class weighting | Balanced |

**Features used:**
`Gls, Ast, G+A, Sh, SoT, TklW, Int, Crs, GA, Saves, Save%, CS, Min, Age`

**Performance Score System:**  
A weighted formula that rates every player based on their position's core duties:

| Position | Primary scoring factors |
|----------|------------------------|
| Forward | Goals ×4, Assists ×2, Shots on Target ×0.5 |
| Midfielder | Goals ×2.5, Assists ×2.5, Tackles Won ×0.8 |
| Defender | Tackles Won ×2.5, Interceptions ×2.5, Goals ×1.5 |
| Goalkeeper | Saves ×1.5, Clean Sheets ×2.0, Save% ×0.3 |

---

## 📈 Visualizations

All 13 charts are saved in the `visuals/` folder. Highlights:

| Chart | Insight |
|-------|---------|
| Top 15 Scorers | League-colored bar chart of the season's best goal scorers |
| Goals vs Assists Scatter | Identifies Pure Scorers, Pure Creators, and Complete Attackers |
| Age Distribution | Prime age zone (23–29) highlighted, median age shown |
| Correlation Heatmap | Relationships between goals, shots, tackles, minutes, and age |
| Confusion Matrix | Shows exactly where the ML model gets predictions right and wrong |
| Performance Scores (2×2) | Top 10 players per position by weighted score |

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/Football-Analytics-DecodeLabs.git
cd Football-Analytics-DecodeLabs
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Update the file path
Open `notebooks/football_analytics_final.ipynb` and update `DATA_PATH` in Cell 4 to match your local path:
```python
DATA_PATH = 'data/players_data_light-2025_2026.csv'
```

### 4. Run the notebook
Open in Jupyter Notebook or VS Code and run all cells from top to bottom.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.11 | Core programming language |
| pandas | Data loading, cleaning, and analysis |
| numpy | Numerical operations and array handling |
| matplotlib | Chart drawing and customization |
| seaborn | Statistical visualizations (boxplot, heatmap) |
| scikit-learn | Machine learning model and evaluation |
| Jupyter Notebook | Interactive development environment |

---

## 📁 Files Description

| File | Format | Description |
|------|--------|-------------|
| `football_analytics_final.ipynb` | `.ipynb` | Complete notebook — all 5 tasks |
| `players_data_light-2025_2026.csv` | `.csv` | Raw dataset (2,779 players) |
| `role_classifier.pkl` | `.pkl` | Trained Random Forest model |
| `scaler.pkl` | `.pkl` | Feature scaler for predictions |
| `label_encoder.pkl` | `.pkl` | Position label encoder |
| `Football_Analytics_Explanation_FINAL.docx` | `.docx` | Full code explanation document |
| `requirements.txt` | `.txt` | Python package dependencies |

---

## 👤 Author

**Mohamed** — Data Science Intern at Decode Labs  
**Internship Period:** 2025–2026  
**Project Focus:** Football / Soccer Data Analytics

---

*Built with ⚽ and Python during the Decode Labs Data Science Internship*
