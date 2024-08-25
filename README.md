## Developed by:Lakshman

## Register no:212222240001

## Date:

# Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (rainfall)

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.

# PROGRAM:

~~~python
import pandas as pd
import matplotlib.pyplot as plt


data = pd.read_csv("/rainfall.csv")

print(data.head)

data['date']=pd.to_datetime(data['date'])

data.set_index('date',inplace=True)
plt.plot(data.index,data['rainfall'],label='rainfall')
plt.title("Daily Minimum rainfall")
plt.xlabel("date")
plt.xticks(rotation=45)
plt.ylabel("rainfall")
plt.grid(True)
plt.legend()
plt.show()
~~~

# OUTPUT:

![Screenshot (1)](https://github.com/user-attachments/assets/b804055b-70a2-4ba0-8758-ac878a13040a)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
