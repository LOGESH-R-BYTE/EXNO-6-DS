# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

import seaborn as sns

import matplotlib.pyplot as plt

df = sns.load_dataset("tips")

df

<img width="693" height="605" alt="image" src="https://github.com/user-attachments/assets/a0152278-903a-4cc2-9e79-bea6c5e009cd" />

sns.lineplot(x="total_bill", y="tip", data=df, hue="sex", linestyle="solid", legend="auto", palette="Set1")

<img width="722" height="552" alt="image" src="https://github.com/user-attachments/assets/31cb9814-eb7a-47e4-8197-e60d21d4c84b" />


x = [1,2,3,4,5]

y1 = [3,5,2,6,1]

y2 = [1,6,4,3,8]

y3 = [5,2,7,1,4]

sns.lineplot(x=x, y=y1)

sns.lineplot(x=x, y=y2)

sns.lineplot(x=x, y=y3)

plt.title("Multi-Line Plot")

plt.xlabel('X Label')

plt.ylabel('Y Label')


<img width="720" height="585" alt="image" src="https://github.com/user-attachments/assets/00c5ce92-09c6-40ca-820e-9f83a8bb34e5" />


tips = sns.load_dataset("tips")

avg_total_bill = tips.groupby("day")["total_bill"].mean()

avg_tip = tips.groupby("day")["tip"].mean()

plt.figure(figsize=(8,6))

p1=plt.bar(avg_total_bill.index, avg_total_bill,label='Total Bill')

p2=plt.bar(avg_tip.index, avg_tip,bottom=avg_total_bill, label='Tip')

plt.xlabel("Day of the week")

plt.ylabel("Amount")

plt.title("Average Total Bill and Tip by Day")

plt.legend()

plt.show()

<img width="723" height="579" alt="image" src="https://github.com/user-attachments/assets/3876c271-574a-4b11-9365-f9c73dd163d8" />


avg_total_bill = tips.groupby("time")["total_bill"].mean()

avg_tip = tips.groupby("time")["tip"].mean()

p1=plt.bar(avg_total_bill.index, avg_total_bill,label='Total Bill',width=0.4)

p2=plt.bar(avg_tip.index, avg_tip,bottom=avg_total_bill, label='Tip',width=0.4)

plt.xlabel("Time of the day")

plt.ylabel("Amount")

plt.title("Average Total Bill and Tip by Time of the Day")

plt.legend()

<img width="693" height="560" alt="image" src="https://github.com/user-attachments/assets/958c939b-96a8-4b6c-b140-97ed696f4a71" />


import seaborn as sns

df = sns.load_dataset("tips")

sns.barplot(x="day", y="total_bill", hue="sex",data=df,palette='Set3')

plt.xlabel("Day of the week")

plt.ylabel("Total Bill")

plt.title("Total Bill by Day and Gender")


<img width="699" height="562" alt="image" src="https://github.com/user-attachments/assets/02891a19-f82d-4e0e-8dac-dcb4095e6329" />


import seaborn as sns

df = sns.load_dataset("tips")

sns.scatterplot(x="total_bill", y="tip", hue="sex",data=df,palette='Set1')

plt.xlabel("Total Bill")

plt.ylabel("Tip")

plt.title("Scatter Plot of Total Bill vs Tip Amount")

<img width="696" height="574" alt="image" src="https://github.com/user-attachments/assets/2f792d65-43ba-4f90-9a49-5d4612d64e81" />


sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette='Set1')

plt.xlabel("Total Bill")

plt.ylabel("Frequency")

plt.title("Distribution of Total Bill by Gender")


<img width="703" height="570" alt="image" src="https://github.com/user-attachments/assets/6eee5bc2-43e5-4cfc-a379-d465c9c27673" />


import seaborn as sns

import pandas as pd

df = sns.load_dataset('tips')

sns.boxplot(x='day', y='total_bill',hue='sex',data=df, palette='Set2')


<img width="703" height="536" alt="image" src="https://github.com/user-attachments/assets/0d77b522-3d30-4a90-a9fa-5ab7626a8f68" />


sns.boxplot(x="day",y="total_bill",hue="smoker",data=df,linewidth=2,width=0.6,fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"},boxprops={"facecolor":"red","edgecolor":"black"},whiskerprops={"color":"darkblue","linestyle":"--","linewidth":"-","linewidth":2},palette="Set1")

<img width="705" height="537" alt="image" src="https://github.com/user-attachments/assets/989c8eb0-0e55-4407-8172-f34f32c2304b" />


sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set1",inner="quartile")

plt.xlabel("Day of the week")

plt.ylabel("Total Bill")

plt.title("Violin Plot of Total Bill by Day and Smoker Status")


<img width="719" height="537" alt="image" src="https://github.com/user-attachments/assets/96011a38-d5c8-403d-868c-c0ded0884f8d" />


import seaborn as sns

sns.set(style="whitegrid")

tip = sns.load_dataset("tips")

sns.violinplot(x="day", y="tip", data=tip, palette="Set2")


<img width="706" height="548" alt="image" src="https://github.com/user-attachments/assets/a384b186-a4ff-4804-a221-85c85a375628" />


import seaborn as sns

sns.set(style="whitegrid")

tip = sns.load_dataset("tips")

sns.violinplot(x=tip["total_bill"],palette="Set1")

<img width="645" height="549" alt="image" src="https://github.com/user-attachments/assets/03c89ffb-2890-41e1-a063-587f4692df59" />

import seaborn as sns

sns.set(style="whitegrid")

tip = sns.load_dataset("tips")

sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")

<img width="733" height="547" alt="image" src="https://github.com/user-attachments/assets/682daf55-7ce6-43e0-aec2-e1f849e2f4cd" />


sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette="Set2",alpha=0.8)

<img width="743" height="555" alt="image" src="https://github.com/user-attachments/assets/ded07785-8ab6-48f6-a972-b27efd675273" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="stack",linewidth=3,palette="Set3",alpha=0.8)

<img width="734" height="553" alt="image" src="https://github.com/user-attachments/assets/b871b480-46a7-497b-8898-ea5de8bea5ec" />


sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="fill",linewidth=3,palette="Set1",alpha=0.8)

<img width="717" height="557" alt="image" src="https://github.com/user-attachments/assets/bf41b3e7-88e1-4e19-b4b7-864e9a4d036d" />


import seaborn as sns

tip = sns.load_dataset("tips")

num = tips.select_dtypes(include=['float64','int64']).columns

corr = tips[num].corr()

sns.heatmap(corr,annot=True,cmap='YlGnBu')

<img width="660" height="523" alt="image" src="https://github.com/user-attachments/assets/f4731134-65ab-458b-9c16-688fa030fc96" />

sns.heatmap(corr,cmap='YlGnBu')

<img width="656" height="529" alt="image" src="https://github.com/user-attachments/assets/6651de64-5e70-4fa2-a365-12649d72ba49" />

# Result:

Thus, the Data Visualization using seaborn python library for the given data executed successfully.
