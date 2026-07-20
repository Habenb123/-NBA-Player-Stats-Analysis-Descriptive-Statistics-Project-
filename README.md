# NBA Player Statistics Analysis (2024 Regular Season)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![Libraries Used](https://img.shields.io/badge/libraries-pandas%20%7C%20numpy%20%7C%20scikit--learn%20%7C%20seaborn%20%7C%20matplotlib-green.svg)](#installation)

An end-to-end sports analytics project executing data scraping, cleaning, feature engineering, exploratory data analysis, visualization, and unsupervised machine learning (K-Means Clustering) on the **2024 NBA regular-season player statistics**.

---

## 📌 Project Overview
Traditional basketball analysis often focuses heavily on simple box-score metrics like Points Per Game (PPG), Assists Per Game (APG), or Rebounds Per Game (RPG). This project uses Python and descriptive statistics to investigate player performance, game-style trends, and roster clusters in detail. 

The data is web-scraped directly from [Basketball Reference](https://www.basketball-reference.com/leagues/NBA_2024_totals.html) and analyzed via a Jupyter Notebook workflow.

---

## 🚀 Key Features

* **Automated Data Scraping:** Scrapes the 2024 player totals dynamically using `pandas`.
* **Robust Data Cleaning:** Handles missing data (e.g., shooting percentages for low-volume players, missing awards) using median and mean imputation methods.
* **Advanced Feature Engineering:** Calculates key advanced performance metrics:
  * **Efficiency Rating (EFF):** Standard league formula assessing multi-categorical contributions.
  * **True Shooting Percentage (TS%):** Overall shooting efficiency metric factoring in 2-pointers, 3-pointers, and free throws.
  * **Scoring / Rebound Rates:** Per-minute scaling (e.g., `PTS_per_min`, `REB_per_min`) to handle playing-time discrepancies.
  * **Assist-to-Turnover Ratio:** Evaluating point guard decision-making quality.
* **Exploratory Data Analysis & Visualizations:** Rich Seaborn and Matplotlib distributions, boxplots, correlation heatmaps, bubble charts, and regression lines mapping player performance.
* **Unsupervised Machine Learning (K-Means Clustering):** Segmenting the league's players into distinct performance-based clusters (e.g., superstars, role players, rim-running specialists) rather than traditional rigid positions (PG, SG, SF, PF, C).

---

## 🛠 Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/nba-player-stats-analysis.git
   cd nba-player-stats-analysis
   ```

2. **Set up a Virtual Environment (Optional but Recommended):**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Open the `NBA PLAYERS STATS ANALYSIS.ipynb` file to run the cells.

---

## 📊 Dataset Columns Details
The scraped dataset initially contains **736 players** and **32 columns** of regular-season performance totals:
* **Rk / Player / Age / Team / Pos / G (Games Played) / GS (Games Started) / MP (Minutes Played)**
* **FG / FGA / FG%** (Field Goals Made/Attempted/Percentage)
* **3P / 3PA / 3P%** (Three-Pointers Made/Attempted/Percentage)
* **2P / 2PA / 2P%** (Two-Pointers Made/Attempted/Percentage)
* **eFG%** (Effective Field Goal Percentage)
* **FT / FTA / FT%** (Free Throws Made/Attempted/Percentage)
* **ORB / DRB / TRB** (Offensive/Defensive/Total Rebounds)
* **AST / STL / BLK / TOV / PF / PTS** (Assists, Steals, Blocks, Turnovers, Personal Fouls, Total Points)
* **Trp-Dbl** (Triple-Doubles)
* **Awards** (Season Awards and All-Star selections)

---

## 📈 Summary of Findings & Visualizations
* **Role Specialization:** Scoring, rebounding, and playmaking lists show clear specialization in the 2024 season (e.g., scoring dominated by guards/wings, rebounding dominated by traditional bigs).
* **Efficiency vs. Scoring:** High volume scorers (like MVP-contenders Luka Dončić and Shai Gilgeous-Alexander) maintain elite True Shooting efficiency, but defensive big men (like Nikola Jokić) dominate overall Efficiency (EFF) metrics due to rebounding and high-percentage field goals.
* **Unsupervised Clustering:** By training a K-Means model on the engineered and raw features, players are grouped dynamically into roles (such as elite volume creators, role-playing floor spacers, and defensive paint anchors) which can be valuable for roster construction.

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an issue.
