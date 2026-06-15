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
