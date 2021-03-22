# Which_Degree
Data analysis to pick he degree based on their job prospec

For this data analysis project, it's been done with Jupyter Notebook so it won't be on Github.


To get the highest Mid-career salary:

import pandas as pd
df = pd.read_csv('/salaries_by_college_major.csv')
clean_df = df.dropna()
clean_df.tail()
print(clean_df['Mid-Career Median Salary'].max())
print(f"Index for the max mid career salary: {clean_df['Mid-Career Median Salary'].idxmax()}")
clean_df['Undergraduate Major'][8]


The Lowest Starting and Mid-Career Salary:

print(clean_df['Starting Median Salary'].min())
clean_df['Undergraduate Major'].loc[clean_df['Starting Median Salary'].idxmin()]


Majors with the Highest Potential :

highest_potential = clean_df.sort_values('Mid-Career 90th Percentile Salary', ascending=False)
highest_potential[['Undergraduate Major', 'Mid-Career 90th Percentile Salary']].head()

