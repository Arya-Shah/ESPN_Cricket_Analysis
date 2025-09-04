🏏 T20 World Cup 2022 Player Analysis
📊 Objective

To analyze T20 World Cup 2022 player performances and build an optimal XI that can:

Score 180 runs in 20 overs

Defend a target of 150 runs in 20 overs

This project combines web scraping, Python (pandas), Bright Data APIs, and Power BI dashboards to provide deep insights into player roles, batting, and bowling performances.

🚀 Features

Automated data extraction from ESPN Cricinfo
 using Bright Data’s Data Collector.

Data transformation with Python (pandas) & Power Query.

20+ custom DAX measures in Power BI for rich, interactive dashboards.

Player classification into Power Hitters, Anchors, Finishers, All-rounders, and Specialist Bowlers.

Selection algorithm for Best XI based on strike rate, batting average, bowling economy, and wicket-taking ability.

📂 Project Workflow
1. Data Collection

Source: ESPN Cricinfo – Match results & player scorecards.

Method: Bright Data’s Data Collector + Python integration.

Extracted JSON data → Transformed into structured datasets.

with open('t20_json_files/t20_wc_match_results.json') as f:
    data = json.load(f)

df_match = pd.DataFrame(data[0]['matchSummary'])


➡️ Match ID created as a key to join scorecard tables.
➡️ Dismissals transformed into out/not out for batting analysis.

2. Data Transformation

Used pandas for joins, cleanup, and feature engineering.

Applied Power Query for filtering, conditional columns, and formatting.

Created calculated fields like:

Boundary %

Balls Faced

Match Phase (Qualifiers vs Super 12)

3. Dashboarding

Built in Power BI with:

Role-based tabs: Power Hitters, Anchors, Finishers, All-rounders, Bowlers.

Interactive filters to compare players.

Scatter plots for Batting Avg vs Strike Rate.

Treemaps & bar charts for bowling styles and wicket distribution.

20+ DAX measures (e.g., Team Strike Rate, Boundary %, Bowling Avg).

🏏 Algorithm for Selecting XI
Role	Criteria	Players Selected
Openers (2)	High strike rate & boundary %	✅
Middle Order (3)	Balance of avg & stability	✅
Finisher (1)	High SR in death overs	✅
All-Rounders (2)	Balance batting + bowling	✅
Specialist Bowlers (3)	Low economy + strike rate	✅

📌 Screenshots below illustrate player analysis and team-building steps.

📸 Dashboards & Visuals
🔥 Power Hitters / Openers

⚖️ Anchors

💥 Finishers

🌀 All Rounders

🎯 Specialist Fast Bowlers

🏆 Final XI – Custom Team Builder

<img width="1920" height="1200" alt="Screenshot 2024-12-30 182550" src="https://github.com/user-attachments/assets/1edd0f73-079e-4ba8-a300-1d671123605d" />
<img width="1920" height="1200" alt="Screenshot 2024-12-30 182621" src="https://github.com/user-attachments/assets/7e8c9212-7dec-4e2f-830d-f827e4fb36ce" />
<img width="1920" height="1200" alt="Screenshot 2024-12-30 182640" src="https://github.com/user-attachments/assets/fc6a2c54-583a-4f4d-9283-61ed46e5e395" />
<img width="1920" height="1200" alt="Screenshot 2024-12-30 182700" src="https://github.com/user-attachments/assets/456b5772-24ac-4d9e-a658-3ebbdc57c38f" />
<img width="1920" height="1200" alt="Screenshot 2024-12-30 182720" src="https://github.com/user-attachments/assets/389ebc2f-5700-4125-9714-9dcb05e584e4" />
<img width="1920" height="1200" alt="Screenshot 2024-12-30 182736" src="https://github.com/user-attachments/assets/8639be19-f38d-496c-9b58-d27640d8d1c0" />
<img width="1251" height="665" alt="Screenshot 2024-12-30 123205" src="https://github.com/user-attachments/assets/56ca4dd6-92c1-450c-bbef-8a6b2ebd9d60" />


⚙️ Tech Stack

Python: pandas, requests, json, python-dotenv

Web Scraping: Bright Data (Data Collector API)

Power BI: DAX, Power Query

Data Source: ESPN Cricinfo (Match Results, Scorecards)

📊 Final XI Team Performance (Sample Output)

Team Strike Rate: 154.54

Team Batting Avg: 39.60

Avg Balls Faced: 19.71

Bowling Avg: 14.12

Bowling Strike Rate: 13.09

Boundary %: 60.10%

🔮 Future Improvements

Automate data pipeline with Airflow.

Include Win Probability Models.

Extend to ODI & Test match formats.

🙌 Acknowledgements

ESPN Cricinfo
 for cricket datasets.

Bright Data
 for proxy-based scraping.

Open-source Python & Power BI community.

