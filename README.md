# Name:Soundarya J
# Reg no :212223220108
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
```
import seaborn as sns
import matplotlib.pyplot as plt
df = sns.load_dataset("tips")
df
```

<img width="367" height="316" alt="image" src="https://github.com/user-attachments/assets/9cb2db87-6d7a-4633-b8fa-1ea8d2b8a3fd" />

```
sns.lineplot(x="total_bill", y="tip", data=df, hue="sex", linestyle="solid", legend="auto", palette="Set1")
```

<img width="562" height="433" alt="download" src="https://github.com/user-attachments/assets/7570b11e-2158-40c7-b2b4-f13047ba5861" />

```
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
```

<img width="554" height="455" alt="download" src="https://github.com/user-attachments/assets/be8e63b9-11fa-4535-a273-d237d162a80f" />

```
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
```

<img width="686" height="547" alt="download" src="https://github.com/user-attachments/assets/d1bed287-750a-4fd9-8469-a6d2e4aa4ac2" />

```
avg_total_bill = tips.groupby("time")["total_bill"].mean()
avg_tip = tips.groupby("time")["tip"].mean()
p1=plt.bar(avg_total_bill.index, avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index, avg_tip,bottom=avg_total_bill, label='Tip',width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
```

<img width="562" height="455" alt="download" src="https://github.com/user-attachments/assets/92829b4b-89ff-4587-a427-b8dc446d3d7d" />

```
import seaborn as sns
df = sns.load_dataset("tips")
sns.barplot(x="day", y="total_bill", hue="sex",data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```

<img width="562" height="455" alt="download" src="https://github.com/user-attachments/assets/724a0ba3-57d3-4762-be79-1d4031ed791e" />

```
import seaborn as sns
df = sns.load_dataset("tips")
sns.scatterplot(x="total_bill", y="tip", hue="sex",data=df,palette='Set1')
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```

<img width="562" height="455" alt="download" src="https://github.com/user-attachments/assets/46ce0890-e57b-41ae-930f-e4f297398005" />

```
sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette='Set1')
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```

<img width="562" height="455" alt="download" src="https://github.com/user-attachments/assets/1463c540-1c17-4eee-9c21-fa954c286072" />

```
import seaborn as sns
import pandas as pd
df = sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill',hue='sex',data=df, palette='Set2')
```

<img width="563" height="432" alt="download" src="https://github.com/user-attachments/assets/9b30c840-c636-418b-88ab-3378df36ad4c" />

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=df,linewidth=2,width=0.6,fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"},boxprops={"facecolor":"red","edgecolor":"black"},whiskerprops={"color":"darkblue","linestyle":"--","linewidth":"-","linewidth":2},palette="Set1")
```

<img width="563" height="432" alt="download" src="https://github.com/user-attachments/assets/4775e7b4-0fe8-44e3-9cc2-3727baf38ce1" />

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set1",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

<img width="572" height="441" alt="download" src="https://github.com/user-attachments/assets/7fdc68b9-8116-49ff-a214-e3fca363180f" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x="day", y="tip", data=tip, palette="Set2")
```

<img width="572" height="441" alt="download" src="https://github.com/user-attachments/assets/e6d01385-f1de-44a0-a52a-414e25dde4ed" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x=tip["total_bill"],palette="Set1")
```

<img width="515" height="441" alt="download" src="https://github.com/user-attachments/assets/317b4dbe-eb01-4c6b-8616-39a11f37e239" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")
```

<img width="587" height="441" alt="download" src="https://github.com/user-attachments/assets/f2876128-2bf3-483c-b62e-27b16dcf0af1" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette="Set2",alpha=0.8)
```

<img width="596" height="441" alt="download" src="https://github.com/user-attachments/assets/2da28c2d-7d7e-4b4d-9fb6-980505d4ab62" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="stack",linewidth=3,palette="Set3",alpha=0.8)
```

<img width="586" height="441" alt="download" src="https://github.com/user-attachments/assets/64e3486e-6ad9-4ca8-9426-6f9dfee26498" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="fill",linewidth=3,palette="Set1",alpha=0.8)
```

<img width="577" height="447" alt="download" src="https://github.com/user-attachments/assets/ee24b927-3594-41e6-956d-7233bfb321f6" />

```
import seaborn as sns
tip = sns.load_dataset("tips")
num = tips.select_dtypes(include=['float64','int64']).columns
corr = tips[num].corr()
sns.heatmap(corr,annot=True,cmap='YlGnBu')
```

<img width="526" height="424" alt="download" src="https://github.com/user-attachments/assets/1645240a-468f-43f8-b24a-ac46971efdd3" />

```
sns.heatmap(corr,cmap='YlGnBu')
```
<img width="526" height="424" alt="download" src="https://github.com/user-attachments/assets/6de2e507-3908-4bad-b650-e90183734939" />



# Result:
 Thus, the Data Visualization using seaborn python library for the given data executed successfully.


