# Main-craft-task1
print("Data Science/Analysis with Python Internship– Task 1")
# output: Data Science/Analysis with Python Internship– Task 1
import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt
# importing libraries 
df= pd.read_csv("/content/dataset.csv")
df
 

2.
df.isnull().mean()
# how many values are null in dataset
 

df.drop_duplicates() # deleting duplicates from dataset 
df.shape # defining shape of the table
df.dtypes # defining datatypes

 
 
 



3.

average_of_math_score =df['math score'].mean()
average_of_math_score
average_of_reading_score =df['reading score'].mean()
average_of_reading_score
average_of_writing_score =df['writing score'].mean()
average_of_writing_score
                         OR

above_15=df[df['math score']>15].mean(numeric_only=True)
above_15

 
above_15=df[df['math score']>15]
print(above_15.shape[0])
avg_by_gender=df.groupby("gender")['math score'].mean()
avg_by_gender

 
4.
plt.figure()
plt.hist(df['math score'])
 
plt.hist(df['reading score'])


 
plt.xlabel("final grade")
plt.ylabel("frequency")
plt.show()


 
plt.hist(df['gender'])

 
plt.bar(avg_by_gender.index,avg_by_gender.values)
plt.xlabel("gender")
plt.ylabel("average math score")
plt.show()
 
Output:


