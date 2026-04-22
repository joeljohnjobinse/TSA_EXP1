# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 22/04/2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv('gld_price_data.csv')

print(data.head())

data['Date'] = pd.to_datetime(data['Date'])

data.set_index('Date', inplace=True)

mean_value = data['GLD'].mean()
print("Mean Value:", mean_value)

plt.figure(figsize=(10, 5))
plt.plot(data.index, data['GLD'], label='GLD Price')

plt.title('Time Series Plot of GLD Price')
plt.xlabel('Date')
plt.ylabel('Price')
plt.legend()

plt.show()
```


# OUTPUT:

<img width="918" height="608" alt="image" src="https://github.com/user-attachments/assets/0d6fc8a2-59c2-4925-9ee7-d7ba8cd8f359" />




# RESULT:
Thus we have created the python code for plotting the time series of given data.
