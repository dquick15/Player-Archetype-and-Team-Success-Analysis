# Player-Archetype-and-Team-Success-Analysis
Descriptive and Predictive Analysis of Player Archetypes and their Correlation to Team Win Success based on 10 NBA seasons of data.


# NBA Player Archetypes and Team Success Analysis

## Project Overview

This project analyzes NBA player statistics to identify distinct player archetypes using K-Means clustering and then investigates how the composition of these archetypes on a team influences team winning percentages across the 2015 - 2025 seasons.

**Key Questions Addressed:**
* What are the fundamental player archetypes based on per-game statistics?
* How do specific player archetypes correlate with team winning percentages?
* What combinations or ratios of archetypes appear to contribute to higher team success?

## Data Sources

The analysis utilizes two primary datasets:
1.  **`Player Per Game.csv`**: Contains individual player per-game statistics (e.g., points, rebounds, assists, shooting percentages) for NBA seasons 2015-2025.
2.  **`Team Summaries.csv`**: Provides team-level summary statistics, including wins and losses, used to calculate winning percentages.

## Methodology

1.  **Data Loading & Preprocessing**:
    * Player statistics were filtered for the 2015- 2025 seasons.
    * Players with less than 10 games played or 5 minutes per game were excluded to ensure a minimum playing time threshold.
    * Relevant statistical features (e.g., `mp_per_game`, `pts_per_game`, `fg_percent`, etc.) were selected.
2.  **Feature Scaling**: Player statistics were standardized using `StandardScaler` to ensure all features contribute equally to the clustering process.
3.  **K-Means Clustering**:
    * K-Means was applied with `n_clusters = 4` to group players into distinct archetypes.
    * The four identified archetypes were named: "Efficient Role Player", "Offensive Engine", "3pt Specialist", and "Interior Force".
4.  **Team Composition Analysis**:
    * The `Team Summaries.csv` was processed to derive team winning percentages.
    * Player archetypes were aggregated by team and season to understand the composition of each team's roster in terms of archetypes.
5.  **Correlation and Combination Analysis**:
    * Correlations between the count of each archetype on a team and the team's winning percentage were calculated.
    * Visualizations (box plots, scatter plots) were created to explore these relationships and analyze archetype ratios (e.g., Offensive Engine to Interior Force ratio) to identify successful team compositions.

## Key Results & Insights

* **Archetype Correlations**:
    * `Efficient Role Player`: 0.082645
    * `Offensive Engine`: -0.12025
    * `3pt Specialist`: -0.305731
    * `Interior Force`: -0.239714
    * *Insight:* A higher number of 'Interior Force' players shows the strongest negative correlation with team winning percentage, suggesting that teams heavily reliant on this archetype may struggle.

* **Top Performing Teams' Archetype Composition**:
    

* **Visualizations**:
    * Box plots show how win percentages vary with the count of each archetype

