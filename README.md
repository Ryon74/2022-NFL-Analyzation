NFL 2022 Season Analysis
Overview
This project analyzes the 2022 NFL season data to evaluate quarterback and running back performance under specific offensive formations and defensive alignments. The analysis focuses on play outcomes, such as average play results, and visualizes the performance of key players and teams using bar charts. Additionally, it examines receiver performance in the first quarter versus later quarters to identify trends in receptions after strong starts.
Project Structure

Data Sources:
plays.csv: Contains play-by-play data for the 2022 NFL season, including quarterback names, offensive formations, and play results.
konbert-output-d1a66dc5.csv: Includes data on running back performance, defensive alignments (e.g., defenders in the box), and team-level play results.


Main Script: projectNFL.ipynb (Jupyter Notebook)
Processes the data, extracts relevant features (e.g., quarterback names, formations), and generates performance metrics and visualizations.


Dependencies:
Python 3.x
Libraries: pandas, numpy, matplotlib


Outputs:
Console outputs of top performers (e.g., quarterbacks in Shotgun/No Huddle, running backs with 6/7/8 defenders in the box).
Bar charts visualizing:
Top 10 quarterbacks in Shotgun and No Huddle formations.
Team and player averages for running plays with 6, 7, or 8 defenders in the box.
Receiver receptions per quarter, comparing season averages to performance after strong first quarters.





Key Features

Quarterback Performance Analysis:

Extracts quarterback names from play descriptions and filters for a predefined list of valid quarterbacks.
Analyzes average play results in Shotgun and No Huddle formations.
Outputs top 10 performers and visualizes results for all quarterbacks.


Running Back Performance Analysis:

Filters plays with 6, 7, or 8 defenders in the box and evaluates running back performance.
Computes average play results for individual running backs and teams.
Visualizes top 5 running backs and team averages for each defensive alignment.


Receiver Performance Analysis:

Identifies pass plays and extracts receiver data for the first quarter versus quarters 2–4.
Compares season-average receptions per quarter to receptions after a strong first quarter (defined as 2+ receptions in Q1).
Visualizes the comparison and calculates whether players perform better with or without a strong first quarter.



Setup Instructions

Clone the Repository:
git clone https://github.com/your-username/nfl-2022-analysis.git
cd nfl-2022-analysis


Install Dependencies:
pip install pandas numpy matplotlib


Prepare Data:

Place plays.csv and konbert-output-d1a66dc5.csv in the project directory.
Ensure the files match the expected format (e.g., columns like playDescription, playResult, ballCarrierDisplayName).


Run the Analysis:

Open projectNFL.ipynb in Jupyter Notebook or Google Colab.
Execute the cells sequentially to process the data and generate outputs.
Alternatively, convert the notebook to a Python script and run it:jupyter nbconvert --to script projectNFL.ipynb
python projectNFL.py





Usage

Run the notebook to generate performance metrics and visualizations.
Modify the valid_qbs_list, valid_ball_carriers, or reciever_names lists in the script to analyze different players.
Adjust the filtering criteria (e.g., quarters, formations, defenders in the box) to explore other scenarios.

Results

Quarterbacks: Top performers in Shotgun and No Huddle formations are identified based on average play results.
Running Backs: Top 5 running backs and team averages are reported for plays with 6, 7, or 8 defenders in the box.
Receivers: Analysis shows how many players perform better with or without a strong first quarter, with a bar chart comparing season averages to post-strong-Q1 performance.

Limitations

The dataset is limited to the 2022 NFL season and specific CSV files.
The analysis assumes accurate play descriptions and consistent data formatting.
Some players may have limited data (e.g., due to injuries or fewer plays), affecting their averages.
The receiver analysis normalizes quarters 2–4 by dividing by 3, which may oversimplify performance trends.

Future Improvements

Incorporate additional seasons for a broader analysis.
Add statistical tests to validate performance differences (e.g., t-tests for receptions).
Include more advanced visualizations, such as heatmaps or player-specific trends over time.
Automate data preprocessing to handle missing or inconsistent data.

