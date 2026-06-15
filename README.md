# 🏏 IPL 2026 Analytics Dashboard

An interactive Power BI dashboard built using IPL 2026 ball-by-ball and match-level data to analyze team performance, batting impact, bowling effectiveness, and venue intelligence.

This project transforms raw cricket datasets into actionable insights through advanced KPIs, custom analytics metrics, and interactive visualizations.

---

## 📌 Project Overview

The dashboard provides a complete analytical view of the IPL 2026 season by combining:

- Match-level statistics
- Ball-by-ball delivery data
- Batting performance
- Bowling performance
- Team standings
- Venue intelligence

The goal was to create a professional sports analytics dashboard that goes beyond traditional scorecards and highlights meaningful patterns within the tournament.

---

## 📊 Dashboard Pages

### 1️⃣ Executive Overview

Provides a high-level summary of the tournament.

#### Key Metrics

- Total Runs
- Total Wickets
- Total Sixes
- Total Fours
- Total Matches
- Average First Innings Score

#### Visuals

- Team Win Rate Analysis
- Tournament Run Trend
- Toss Winner Analysis
- Tournament KPI Cards

---

### 2️⃣ Batting Intelligence

Analyzes batting performance across players and teams.

#### Key Metrics

- Total Runs
- Batting Average
- Strike Rate
- Total Fours
- Total Sixes

#### Visuals

- Batter Impact Matrix (Average vs Strike Rate)
- Runs Scored by Match Phase
- Boundary Analysis
- Top Performing Batters

---

### 3️⃣ Bowling Intelligence

Evaluates bowling efficiency and wicket-taking ability.

#### Key Metrics

- Total Wickets
- Economy Rate
- Dot Ball Percentage
- Maiden Overs

#### Visuals

- Bowling Quadrant (Economy vs Wickets)
- Wickets by Match Phase
- Top Wicket Takers
- Bowling KPI Cards

---

### 4️⃣ Team Intelligence

Provides insights into team-level performance.

#### Metrics

- Win Percentage
- Team Rankings
- Overall Tournament Performance

#### Visuals

- Team Win Rate Comparison
- Team Performance Analysis

---

### 5️⃣ Venue Intelligence

Analyzes venue behavior and scoring patterns.

#### Custom Analytics Metrics

##### Venue Difficulty Index

Measures whether a venue favors batters or bowlers by comparing venue average score with tournament average score.

##### Boundary Dependency %

Measures the percentage of total runs scored through boundaries.

#### Visuals

- Venue Difficulty Index
- Average Venue Score Ranking
- Bat First vs Chase Wins
- Boundary Dependency Analysis
- Venue Profile Dashboard

---

## ⚙️ Data Sources

The project uses the following datasets:

- deliveries.csv
- matches.csv
- batting_stats.csv
- bowling_stats.csv
- fielding_stats.csv
- points_table.csv
- venues.csv
- squads.csv

The dataset contains match-level and ball-by-ball data for IPL 2026.

---

## 🛠️ Tools & Technologies

- Power BI
- DAX
- Data Modeling
- Data Visualization
- Sports Analytics

---

## 📈 Key DAX Measures

Examples of custom measures used:

### Total Runs

```DAX
Total Runs =
SUM(deliveries[runs_of_bat]) +
SUM(deliveries[extras])
```
###Dot Ball %
```
Dot Ball % =
DIVIDE(
SUM(bowling_stats[dot_balls]),
SUM(bowling_stats[balls])
) * 100
```
###Venue Difficulty Index
```
Venue Difficulty Index =
DIVIDE(
AVERAGE(matches[first_ings_score]),
CALCULATE(
AVERAGE(matches[first_ings_score]),
ALL(matches[venue])
)
)
Boundary Dependency %
Boundary Dependency % =
DIVIDE(
[Boundary Runs],
[Total Runs]
) * 100
```
🎯 Business Questions Answered
Which teams performed best during IPL 2026?
Which batters combined high averages with aggressive strike rates?
Which bowlers balanced wicket-taking ability with economy?
Which venues favored batting and which favored bowling?
Which venues produced the highest scoring matches?
How important were boundaries in venue scoring patterns?
Did teams have more success batting first or chasing?
📷 Dashboard Screenshots
Executive Overview


<img width="1432" height="808" alt="Screenshot 2026-06-14 113417" src="https://github.com/user-attachments/assets/4a64cdf2-e693-4d53-9eda-59eb8c12f1b8" />


Batting Intelligence
<img width="1430" height="851" alt="Screenshot 2026-06-14 113504" src="https://github.com/user-attachments/assets/943649b5-7a90-4cbc-81fd-d0641a1aa17c" />



Bowling Intelligence
<img width="1432" height="846" alt="Screenshot 2026-06-14 113526" src="https://github.com/user-attachments/assets/da5c4226-3c25-43c6-be85-50699f2ccc6b" />



Team Intelligence
<img width="1417" height="851" alt="image" src="https://github.com/user-attachments/assets/8278ff5b-20ca-44c4-95d5-40caf5b7a1a7" />



Venue Intelligence
<img width="1435" height="851" alt="Screenshot 2026-06-14 113609" src="https://github.com/user-attachments/assets/185af4cd-c5ad-4db2-8e4b-e519cd923bf3" />



##🚀 Future Improvements
-Player profile drill-through pages
-Predictive match outcome analysis
-Advanced player impact scoring
-Venue clustering and segmentation
-Team attack and defense ratings

##👨‍💻 Author

Dushyant Singh Jadon

Aspiring Data Analyst | Power BI Developer | Sports Analytics Enthusiast
