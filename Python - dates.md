[[Python]]

## Python - dates

import datetime

today = datetime.date.today()

print(today)  # 2020-09-19  
print(type(today))  # <class 'datetime.date'>

year = today.year  
month = today.month  
day = today.day

print(year)  # 2020  
print(month)  # 9  
print(day)  # 19

From <[https://www.atqed.com/python-today](https://www.atqed.com/python-today)>

--------------------

You can use

pd.Timestamp('today')

or

pd.to_datetime('today')

But both of those give the date and time for 'now'.

Try this instead:

pd.Timestamp('today').floor('D')

or

pd.to_datetime('today').floor('D')

You could have also passed the datetime object to pandas.to_datetime but I like the other option mroe.

pd.to_datetime(datetime.datetime.today()).floor('D')

Pandas also has a Timedelta object

pd.Timestamp('now').floor('D') + pd.Timedelta(-3, unit='D')

Or you can use the offsets module

pd.Timestamp('now').floor('D') + pd.offsets.Day(-3)

To check for membership, try one of these

cur_date in df['date'].tolist()

Or

df['date'].eq(cur_date).any()

From <[https://stackoverflow.com/questions/51827134/comparison-between-datetime-and-datetime64ns-in-pandas](https://stackoverflow.com/questions/51827134/comparison-between-datetime-and-datetime64ns-in-pandas)>