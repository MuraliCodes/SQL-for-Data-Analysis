# 🏏 IPL Data Analysis with SQL 

This project demonstrates how to perform "Data Analysis on IPL match data" using sql queries.

# 📂 Dataset

-File Name : IPL_Matches.csv

-Sourse : Contains historical IPL match data including teams, venues, toss, results, and player awards.

# 🛠️ Technologies Used

-Python

-Pandas

=SQLite3

-Google Colab 

# 🛠️ Technologies Used

1.Upload 'IPL_Matches.csv' to colab session

2.Run the following setup:

---python
import pandas as pd
import sqlite3

#Load dataset

ipl_df = pd.read_csv('IPL_Matches.csv')

#Create SQLite DB

conn = sqlite3.connect(':memory:')

ipl_df.to_sql('ipl_matches',conn,index=False,if_exists='replace')
