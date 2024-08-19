# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 17-08-24

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
Developed by: Marella Dharanesh
REGISTER NO: 212222240062
```
```
import pandas as pd
import matplotlib.pyplot as plt

file_path = 'daily-minimum-temperatures-in-me.csv'
data = pd.read_csv(file_path)

print(data.head)

data['Date']=pd.to_datetime(data['Date'])

data.set_index('Date',inplace=True)
plt.plot(data.index,data['temp'],label='temp')
plt.title("Daily Minimum Temperature")
plt.xlabel("Date")
plt.xticks(rotation=45)
plt.ylabel("Temperature")
plt.grid(True)
plt.legend()
plt.show()

```



# OUTPUT:
![Screenshot 2024-08-16 220358](https://github.com/user-attachments/assets/9baa26a5-d9b0-484a-8de1-354907cbae86)






# RESULT:
Thus we have created the python code for plotting the time series of given data.
