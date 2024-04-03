# Ex.No: 05  IMPLEMENTATION OF TIME SERIES ANALYSIS AND DECOMPOSITION
### Date: 23/3/24


### AIM:
To Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the decomposition process for the required data.
4. Plot the data according to need, either seasonal_decomposition or trend plot.
5. Display the overall results.

### PROGRAM:
~~~
!pip install pandas

import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose

# Load dataset (replace with your data)
data = pd.read_csv('/content/Temperature.csv')

# Convert 'date' column to datetime format and set as index
data['Month'] = pd.to_datetime(data['Month'])
data.set_index('Month', inplace=True)

# Specify the period for decomposition
period = 12  # Change this to the appropriate period for your data

# Perform decomposition
result = seasonal_decompose(data, model='multiplicative', period=period)

# Plot the decomposition
result.plot()
plt.show()
~~~
















### OUTPUT:
![](https://private-user-images.githubusercontent.com/94165064/316245372-cbf97321-ad8e-4238-8ead-31fea131cde3.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTIxNDA1NzcsIm5iZiI6MTcxMjE0MDI3NywicGF0aCI6Ii85NDE2NTA2NC8zMTYyNDUzNzItY2JmOTczMjEtYWQ4ZS00MjM4LThlYWQtMzFmZWExMzFjZGUzLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA0MDMlMkZ1cy1lYXN0LTElMkZzMyUy)



### RESULT:
Thus we have created the python code for the time series analysis and decomposition.
