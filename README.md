# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

## Name : HIRUTHIK SUDHAKAR
## Roll : 212223240054

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
```python
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![326680557-f83d445f-47d6-4030-b1ac-349061d8446f](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/47a2e1f8-e225-45cb-a7c9-5845074d3aad)
### 1.Line Plot
```python
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![326680593-ff29a7a6-f9c5-48e2-aadf-a5df5adcf617](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/f4661ac2-18df-48dc-a7ca-7a114a814982)
### 2.Multiline Plot
```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![326680637-fce23053-5339-4aa1-b2e2-6b149cf3f90a](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/db486ae1-6a73-42ce-91ca-6735e21385e2)
## To Visualize Relationships
### 1.Bar Chart
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![326680678-554517c7-0025-40c9-91dd-1cc251d7d769](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/2c03d7a2-8ff7-439d-a4fc-96b9f13b37e9)
### 2.Scatter Plot
```python
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![326680727-5cb1073f-df00-4730-8b0d-c9b3ad5a91e5](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/053d3744-0f30-4bb2-81cf-b4e6df636fd7)
### 3.Bubble Chart
```python
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![326680801-8d9a4978-7b71-4d03-9c2e-1cc8e84a8c42](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/b99f15e3-035f-4aaa-896a-9def7b615466)
## To Capture Distributions
### 1.Histogram
```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![326680844-f9e5f588-347b-414d-adcf-c4e97327cfc8](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/ede434fc-8f91-49d3-bc11-0a52f8e02bde)
### 2.Box Plot
```python
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![326680887-ddadf567-47bb-40e7-9cea-28cc4eec3c18](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/edb99c5d-6ff1-41ad-8b6b-5da4534b2e02)
### 3.Violin Plot
``` python
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![326680921-e4e84071-4cfd-411e-9ef4-c87f1ba820bb](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/c929293c-f666-4c12-a55a-ea9ea52015bc)
### 4.Density Plot
``` python
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![326680960-80cfb121-4f96-442b-ab9e-43559a91c92e](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/31881338-ee40-462c-bf3c-bac603598c9a)
### 5.Heatmap
``` python
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![326680978-bea2b9f0-618d-42cf-a46b-5a44b7e46292](https://github.com/KesavDeepak/EXNO-6-DS/assets/139336019/9636642e-b953-43ec-afc8-fc58883c158b)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
