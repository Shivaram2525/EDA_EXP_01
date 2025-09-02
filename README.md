# Experiment 1: EDA in IPL Dataset
```
Name     : Shivaram M.
Reg. No. : 212223040195
```
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

### 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
### 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
### 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
### 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
### 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
### 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
### 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
## Program
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
matches=pd.read_csv('/Users/home/Desktop/Workspace/College/Semester_5/EDA/Experiments/EXP_1/Dataset/matches.csv')
print("Dataset Shape:", matches.shape)
print(matches.head())
season_counts=matches['season'].value_counts().sort_index()
print("\nMatches per season:\n", season_counts)
plt.figure(figsize=(8,4))
sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
plt.title("Number of Matches per Season")
plt.xlabel("Season")
plt.ylabel("Matches")
plt.show()

```

## Output

<img width="1680" height="1050" alt="1" src="https://github.com/user-attachments/assets/47f3edf4-1ab7-44a4-957e-a09143a66a9b" />
<img width="1680" height="1050" alt="2" src="https://github.com/user-attachments/assets/c32236c6-e7ee-4cb6-9394-5aa46a6ecec2" />
<img width="1680" height="1050" alt="3" src="https://github.com/user-attachments/assets/c56e36b0-7d28-4530-8792-7b0ced262468" />
<img width="1680" height="1050" alt="4" src="https://github.com/user-attachments/assets/b7b154b7-fb85-4550-b0f6-910eaf3e4789" />


## Result
  This experiment is executed successfully
