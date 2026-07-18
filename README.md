# 🏀 NBA Player Performance Analysis
### Evolution of 3-Point Shooting & Scoring Efficiency (2010–2025)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Charts-4C72B0)

**Domain:** Sports Analytics — NBA
**Dataset:** NBA Player Stats and Salaries, 2010–2025 (Kaggle)
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn

---

## 📌 Problem Statement

The NBA has undergone a significant transformation over the past 15 years. Teams and players have increasingly shifted from traditional 2-point scoring to 3-point shooting. This project analyzes how 3-point shooting and scoring efficiency evolved from 2010 to 2025, and identifies which players, positions, and seasons drove that change.

### Research Questions
1. How much have 3-point attempts increased over the years?
2. Which positions adopted 3-point shooting the most?
3. Who are the most efficient and highest-volume 3-point shooters?
4. Does scoring efficiency (eFG%) correlate with salary?
5. At what age do players statistically peak?
6. Which teams lead the league in pace, efficiency, and scoring?

---

## 🗂️ Dataset

| Column | Description |
|--------|-------------|
| Player | Player name |
| Salary | Annual salary (USD) |
| Year | Season year |
| Pos | Position (PG, SG, SF, PF, C) |
| Age | Player age |
| Team | Team abbreviation |
| G, GS, MP | Games played, games started, minutes/game |
| FG, FGA, FG% | Field goals made, attempted, % |
| 3P, 3PA, 3P% | 3-pointers made, attempted, % |
| 2P, 2PA, 2P% | 2-pointers made, attempted, % |
| eFG% | Effective field goal % |
| FT, FTA, FT% | Free throws made, attempted, % |
| ORB, DRB, TRB | Offensive, defensive, total rebounds |
| AST, STL, BLK | Assists, steals, blocks |
| TOV, PF, PTS | Turnovers, fouls, points per game |

**Rows:** ~7,300 player-seasons | **Seasons covered:** 2010–2025

### Data Cleaning
- Filled `NaN` percentage columns (e.g. `3P%`) with `0` for players who never attempted that shot type
- Standardized multi-position labels (e.g. `PG-SG`) to a single primary position
- Removed low-minute players (`G < 10`) that skew percentage stats
- Excluded the incomplete 2025 season from year-over-year trend analysis
- Added an `Era` label for era-based comparisons:
  - **Pre-Revolution:** 2010–2014
  - **Transition:** 2015–2019
  - **3PT Dominant:** 2020–2025

---

## 📊 Key Findings

| Metric | 2010 | 2024 | Change |
|---|---|---|---|
| Avg 3-Point Attempts / game | 1.62 | 2.89 | **+78.6%** |
| League Effective FG% | 49.1% | 53.8% | **+4.7 pts** |
| Center Avg 3PA / game | 0.24 | 0.96 | **4x increase** |
| Share of shots that are 3-pointers | ~23.4% | ~39.5% | **Nearly doubled** |
| Avg NBA Salary | $4.62M | $9.91M | **+114.4%** |

- The NBA has undergone a **massive 3-point revolution** — attempts nearly doubled over 15 seasons.
- **Scoring efficiency (eFG%)** improved steadily as teams embraced smarter shot selection.
- **All positions** adopted the 3-pointer, most dramatically Centers, who went from almost never shooting from deep to making it a regular part of their game.
- The **Transition Era (2015–2019)** was the turning point, heavily influenced by the Golden State Warriors dynasty and Stephen Curry's influence.
- Shot share shifted from roughly 23% to 40% 3-point attempts, fundamentally changing how basketball is played.
- **Salary correlates loosely with performance** — high scorers tend to earn more, but efficiency alone doesn't guarantee top pay.
- Players statistically peak in **points per game around age 28** and in **effective FG% around age 27**.

---

## 📈 Visualizations

### 1. League-Wide 3-Point Revolution Trends (2010–2024)
![League-Wide Trends](images/chart_01.png)

Average 3-point attempts, 3P%, 2-point attempts, and eFG% by season — the clearest view of the leaguewide shift toward the perimeter.

### 2. 2PT vs 3PT Attempts by Era
![2PT vs 3PT by Era](images/chart_02.png)

### 3. Position-wise 3PA Evolution
![3PA by Position](images/chart_03.png)

Every position increased 3-point volume, but Centers and Power Forwards show the steepest relative climb.

### 4. Top 10 Players by 3-Point Volume
![Top 10 3PT Volume](images/chart_04.png)

### 5. Top 10 Most Efficient 3-Point Shooters (Min. 3 Attempts/Game)
![Top 10 3PT Efficiency](images/chart_05.png)

### 6. Top 10 Scorers (2010–2025)
![Top 10 Scorers](images/chart_06.png)

### 7. Correlation Heatmap — Stats & Salary
![Correlation Heatmap](images/chart_07.png)

### 8. eFG% vs Salary — Does Efficiency Earn More Money?
![eFG% vs Salary](images/chart_08.png)

### 9. Points Distribution by Position
![Points by Position](images/chart_09.png)

### 10. Distribution of 3-Point % Across All Players
![3P% Distribution](images/chart_10.png)

### 11. Shot Share (2PT vs 3PT) by Era
![Shot Share by Era](images/chart_11.png)

### 12. Top 10 Highest-Paid Players vs Efficiency
![Highest Paid vs Efficiency](images/chart_12.png)

### 13. Most Improved Players — Year-over-Year
![Most Improved Players](images/chart_13.png)

CJ McCollum's 2016 season (+14.0 PPG) tops the list of biggest single-season scoring jumps.

### 14. NBA Salary Growth Over Seasons (2010–2024)
![Salary Growth](images/chart_14.png)

### 15. Age vs Performance — When Do Players Peak?
![Age vs Performance](images/chart_15.png)

| Metric | Peak Age |
|---|---|
| Points Per Game | 28 |
| Effective FG% | 27 |
| 3-Point % | 40* |
| Assists Per Game | 39* |

*\*Small sample size at older ages inflates these figures.*

### 16. Team-wise Analysis (Pace, Efficiency, Scoring)
![Team-wise Analysis](images/chart_16.png)

The Houston Rockets and New Orleans Pelicans lead the league in average 3-point attempts and points per game respectively, reflecting pace-and-space, high-volume offensive systems.

---

## 🧠 Conclusion

This project analyzed NBA player stats and salary data from 2010 to 2025 to understand the evolution of 3-point shooting and scoring efficiency. The data confirms a clear, sustained "3-point revolution": attempt rates nearly doubled, efficiency climbed leaguewide, and even traditional interior positions like Center adapted their game to include perimeter shooting. The Golden State Warriors-driven Transition Era (2015–2019) marks the inflection point after which 3-point volume became the norm rather than the exception.

### Future Scope
- Incorporate playoff statistics for deeper performance analysis
- Build a machine learning model to predict player salary from performance stats
- Bring in team-level data to analyze how team strategy shaped individual stats
- Extend to game-by-game or quarter/half-level granularity

---

## 📁 Repository Structure
```
.
├── README.md
├── NBA_Analysis.ipynb                              # Full analysis notebook
├── NBA_Player_Stats_and_Salaries_2010-2025.csv     # Source dataset
└── images/                                          # Exported chart images
```

## 🛠️ How to Reproduce
```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook NBA_Analysis.ipynb
```

---

*Dataset source: NBA Player Stats and Salaries 2010–2025 (Kaggle).*
