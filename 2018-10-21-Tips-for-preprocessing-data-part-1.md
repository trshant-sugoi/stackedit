---
layout: post
title: "Code Snippets for data preprocessing using Pandas - Part 1"
date: 2018-10-21T07:51:43+05:30
draft: false
tags : [BigData,pandas,CodeSnippets]
Description : "Code Snippets for data preprocessing using Pandas - Part 1"
---
This post will be all about processing data using pandas.

Use this to read CSVs into a dataframe
```
df = pd.read_csv('train.csv')
```
However, in case you need to prepare a DataFrame and have been unfortunate enough to get a CSV file with no headers, then this is the way to go
```
df = pd.read_csv('file_name.csv', header = None, names = ['labels','you','want','to','give'] )
```
This is one very usable function to see which data is empty or null
```python
def missing_data_table(df):
    total = df.isnull().sum().sort_values(ascending=False)
    percent = (df.isnull().sum()/df.isnull().count()).sort_values(ascending=False)
    missing_data = pd.concat([total, percent], axis=1, keys=['Total', 'Percent'])
    return missing_data
```

If you see any empty data you can fill it in with
```
df['column_name'].fillna(1000, inplace=True)
```

Dropping a column is easy
```
df.drop('column_name', axis=1, inplace=True)
```

Dropping row/s if a column is blank/null
```
df.drop(df[pd.isnull(df['Embarked'])].index, inplace=True)
```

We can make columns categorical ( converting 'male' and 'female' to 0 and 1 ) without too much trouble
```
df['Sex'] = pd.Categorical(df['Sex'])
```

However this wont be seen easily till you  do this bit
```
df = pd.get_dummies(df, drop_first=True)
```

See the dataframe:
```
df.head(optional number of rows you want to see)
```

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc5MDQ0Mzk2OV19
-->