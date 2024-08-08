import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

import seaborn as sns

file_path=r"C:\Users\DELL\Desktop\market.csv"

data=pd.read_csv(file_path)

print(data.shape)
print(df.head())
data.isnull().sum()
data.info()
data.describe()
print("Dataset contains {} row and {} colums".format(data.shape[0],data.shape[1]))
data.groupby(['Gender']). agg({'Total':'sum'})
plt.style.use('ggplot')

plt.figure(figsize= (14,6))

ax = sns.countplot(x = "Customer type", data = data, palette = "rocket_r")
data.groupby(['Customer type']). agg({'Total':'sum'})
plt.figure(figsize=(14,6))

plt.style.use('classic')

ax = sns.countplot(x = "Customer type", hue = "Branch", data = data, palette= "rock

ax.set_title(label = "Customer type in different branch", fontsize = 25)

ax.set_xlabel(xlabel = "Branches", fontsize = 16)

ax.set_ylabel(ylabel = "Customer Count", fontsize = 16)
plt.figure(figsize = (14,6))

ax = sns.countplot(x = "Payment", data = data, palette = "tab20")

ax.set_title(label = "Payment methods of customers ", fontsize= 25)

ax.set_xlabel(xlabel = "Payment method", fontsize = 16)

ax.set_ylabel(ylabel = " Customer Count", fontsize = 16)
ax.set_title("Type of customers", fontsize = 25)

ax.set_xlabel("Customer type", fontsize = 16)

ax.set_ylabel("Customer Count", fontsize = 16)
plt.figure(figsize = (14,6))

plt.style.use('classic')

ax = sns.countplot(x="Payment", hue = "Branch", data = data, palette= "tab20")

ax.set_title(label = "Payment distribution in all branches", fontsize= 25)

ax.set_xlabel(xlabel = "Payment method", fontsize = 16)

ax.set_ylabel(ylabel = "Peple Count", fontsize = 16)
plt.figure(figsize=(14,6))

ax = sns.boxplot(x="Branch", y = "Rating" ,data =data, palette= "RdYlBu")

ax.set_title("Rating distribution between branches", fontsize = 25)

ax.set_xlabel(xlabel = "Branches", fontsize = 16)

ax.set_ylabel(ylabel = "Rating distribution", fontsize = 16)
data["Time"]= pd.to_datetime(data["Time"])

data["Hour"]= (data["Time"]).dt.hour
plt.figure(figsize=(10,6))

plt.style.use('classic')

ax = sns.boxenplot(x = "Quantity", y = "Product line", data = data,)

ax.set_title(label = "Average sales of different lines of products", fontsize = 25)

ax.set_xlabel(xlabel = "Qunatity Sales",fontsize = 16)

ax.set_ylabel(ylabel = "Product Line", fontsize = 16)
plt.figure(figsize=(14,6))

plt.style.use('classic')

SalesTime = sns.lineplot(x="Hour", y ="Quantity", data = data).set_title("product sales per hour")
plt.figure(figsize=(14,6))

plt.style.use('classic')

rating_vs_sales = sns.lineplot(x="Total", y= "Rating", data=data)
plt.figure(figsize=(14,6))

ax = sns.countplot(y='Product line', data=data, order = data['Product line'].value_

ax.set_title(label = "Sales count of products", fontsize = 25)

ax.set_xlabel(xlabel = "Sales count", fontsize = 16)

ax.set_ylabel(ylabel= "Product Line", fontsize = 16)
plt.figure(figsize=(14,6))

plt.style.use('classic')

ax = sns.boxenplot(y= "Product line", x= "Total", data = data)

ax.set_title(label = " Total sales of product", fontsize = 25)

ax.set_xlabel(xlabel = "Total sales", fontsize = 16)

ax.set_ylabel(ylabel = "Product Line", fontsize = 16)
plt.figure(figsize = (14,6))

plt.style.use('classic')

ax = sns.boxenplot(y = "Product line", x = "Rating", data = data)

ax.set_title("Average rating of product line", fontsize = 25)

ax.set_xlabel("Rating", fontsize = 16)

ax.set_ylabel("Product line", fontsize = 16)
plt.style.use('classic')

plt.figure(figsize = (14,6))

ax= sns.stripplot(y= "Product line", x = "Total", hue = "Gender", data = data)

ax.set_title(label = "Product sales on the basis of gender")

ax.set_xlabel(xlabel = " Total sales of products")

ax.set_ylabel(ylabel = "Product Line")
plt.figure(figsize = (14,6))

plt.style.use('classic')

ax = sns.relplot(y= "Product line", x = "gross income", data = data)

