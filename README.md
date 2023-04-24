# Python-datetime-module
Python datetime module

#import libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import datetime
from datetime import date

# read the Dataset
import pandas as pd
df=pd.read_csv("D:\\DATASCIENCE\\DATA SCIENCE\\DATA\\Global Super Store Dataset\\Global Super Store Dataset 10 rows.csv")

df

#dataset information
df.info()


# Convert time stamp column to date time object into date
df["Order Date"] = pd.to_datetime(df["Order Date"])
df.info

#date fomrmat convert into object to date format
df.info()

#extract the date 
df["Order Date"].dt.date


df

df["DATE"] = df["Order Date"].dt.date
df

# Method q - Using .dt.time

df.info()

import time

time.time()

time.ctime(1682309802.7635365)

help(time.time)

time.localtime()

a=time.localtime()
b=time.mktime(a)
print(b)

c=time.asctime(a)
print(c)

help(time.strftime)

print(a)

x=time.strftime("m/%d/%Y")

print(x)

# Date format capital or small change into format small (YY) or Capital (YYYY) 
x=time.strftime("m/%d/%y")

print(x)

# Datetime

import datetime

print(datetime.datetime(2019,6,7,4,30,54,678))

datetime.datetime.today()

datetime.datetime.now()

v=datetime.datetime.now()

v.year

print(v.month)
print(v.hour)

datetime.time(3,45,23)

b1=datetime.timedelta(days=20)
b2=datetime.timedelta(days=30)
b3=b1-b2
print(b3)
print(type(b3))

