# NBA Data Analysis SQL Project

This project contains a set of SQL queries designed to analyze and manipulate NBA data from CSV files. The project focuses on extracting insights from datasets related to teams, games, players, and play-by-play events to better understand player performance, team efficiency, and data relationships within NBA game data.

> **Note:** The file `play_by_play.csv`, used in the analysis, is approximately 2.5GB and is not included in this repository due to its size.

## Project Overview

The primary goals of this project were to:
- **Query Team Data:** Extract details of teams where certain conditions are met, such as matching city and state.
- **Analyze Game Performance:** Identify games with high scoring efficiency by calculating point-to-field-goal and point-to-free-throw ratios.
- **Count Events by Game Period:** Track the number of events (comments) in each period to gain insights into game activity.
- **Identify Key Players:** Retrieve details of the tallest players among the NBA's Greatest 75.
- **Handle Missing Data:** Detect missing player and team data in the play-by-play records to ensure data integrity.

## Key Queries

Some of the SQL queries included:
- **Teams by City and State Match**: Retrieves teams where the city is the same as the state.
- **High Scoring Efficiency Games**: Finds games with high points-per-field-goal and points-per-free-throw ratios.
- **Tallest Players among NBA's Greatest 75**: Lists the tallest players who are part of the NBA’s Greatest 75.
- **Player Count per Team**: Counts the players associated with each team.

## Functional Dependencies

Two main functional dependencies identified in the project:
1. `team_id -> team_name`: In the Players table, `team_id` determines `team_name`. Any changes to a team's name require updates in multiple rows where `team_id` appears.
2. `player1_id -> player1_name, player1_team_id`: In the Play_by_play table, `player1_id` determines `player1_name` and `player1_team_id`. If a player’s name or team changes, all rows with the same `player1_id` must be updated accordingly.

This project showcases practical SQL querying techniques for large datasets and demonstrates how to handle and maintain data accuracy in real-world sports databases.
