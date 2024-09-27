## Developed By: Marella Dharanesh
## Register No: 212222240062
##  Date:  

# Ex.No: 01A  PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (National stock exchange)


# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Use the data column  for tracking the index. 
4. Plot the data accordingly Which can be altered monthly, or yearly.
5. Display the graph.


# PROGRAM:
```python
import pandas as pd
import matplotlib.pyplot as plt
file_path = 'infy_stock.csv'
data = pd.read_csv(file_path)
print(data.head)
data['Date']=pd.to_datetime(data['Date'])
data.set_index('Date',inplace=True)
plt.plot(data.index,data['Trades'],label='temp')
plt.title("Daily Minimum Trades")
plt.xlabel("Date")
plt.xticks(rotation=45)
plt.ylabel("Trades")
plt.grid(True)
plt.legend()
plt.show()
```

# OUTPUT:

![series_1a_1](https://github.com/user-attachments/assets/27e0c27e-a007-437a-bcc4-a0feb60cea68)


![series_1a_2](https://github.com/user-attachments/assets/da59e751-736b-442a-a70e-617e62e9f158)








# RESULT:
Thus the python code has created for plotting the time series of given data Successfully.
