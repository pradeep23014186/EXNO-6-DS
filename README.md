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
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
![image](https://github.com/user-attachments/assets/5fbd02f6-89e8-4f2f-822a-4ff4364cbe7f)

## Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/user-attachments/assets/e80fc810-afde-4032-a573-a06075602720)

## Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/user-attachments/assets/aae54ef5-a99d-4a5b-a2e7-6f70ae70537b)

# TO VISUALIZE RELATIONSHIPS :

## Bar Chart

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/user-attachments/assets/33e611a7-f2b4-4ac0-a2a9-c84c883bc386)

## Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/user-attachments/assets/69e979ab-55f0-4e60-81b5-35878c4b7702)

# TO CAPTURE DISTRIBUTIONS :

## Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/user-attachments/assets/67658d92-ba12-4e63-bd41-26c117c444f1)

## Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/user-attachments/assets/fbec0c64-ca8b-4f62-98f6-e25585e5e75f)

## Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/user-attachments/assets/efd216a6-6d73-459d-a8b0-194771720863)

## Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/user-attachments/assets/234d106d-d390-405a-b08c-7618a457c6be)

## HeatMap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/user-attachments/assets/0f1d296c-61f4-4add-a870-6a6d416c3be5)

# Result:
 Thus, the Data visulaization using seaborn python library for the given data is implemented sucessfully
