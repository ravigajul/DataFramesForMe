# DataFramesForMe

What is a DataFrame?

A DataFrame is like an Excel table or a SQL table — it’s a 2-dimensional tabular data structure made of rows and columns.

It comes from the pandas library in Python (though similar concepts exist in R, Spark, and others).


Basic Structure

Here’s what a DataFrame looks like:

Name	Age	City
Alice	25	New York
Bob	30	San Diego
Carol	22	Chicago

This structure is ideal for:
	•	Viewing data
	•	Manipulating data
	•	Analyzing datasets


Getting Started with Pandas and DataFrames

1. Import Pandas

import pandas as pd

2. Create a DataFrame

You can create a DataFrame from a Python dictionary:

data = {
    'Name': ['Alice', 'Bob', 'Carol'],
    'Age': [25, 30, 22],
    'City': ['New York', 'San Diego', 'Chicago']
}

df = pd.DataFrame(data)
print(df)

Output:

    Name  Age       City
0  Alice   25   New York
1    Bob   30  San Diego
2  Carol   22    Chicago

Key DataFrame Concepts

Concept	Explanation
df.shape	Returns number of rows and columns, e.g., (3, 3)
df.columns	Lists column names
df.head()	Shows the first 5 rows
df.describe()	Summary statistics for numeric columns
df['Age']	Access a single column
df.iloc[0]	Access first row (by index)
df.loc[0]	Access row by label (if using custom index)

Real-World Uses of DataFrames
	•	Reading a CSV file:

df = pd.read_csv('file.csv')


	•	Writing to Excel:

df.to_excel('output.xlsx')


	•	Filtering rows:

df[df['Age'] > 25]


	•	Sorting:

df.sort_values(by='Age', ascending=False)


	•	Adding a new column:

df['Is_Adult'] = df['Age'] >= 18
