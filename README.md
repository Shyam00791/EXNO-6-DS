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
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset (1).csv")
df.head()
```

<img width="812" height="362" alt="image" src="https://github.com/user-attachments/assets/559d0ed7-1eda-417b-aaa5-1230b9599e80" />

```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="515" height="427" alt="image" src="https://github.com/user-attachments/assets/602ebd88-c3b8-4f08-b9d1-591d4a267b25" />

```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="531" height="433" alt="image" src="https://github.com/user-attachments/assets/e9150e22-d271-4c53-8051-dbab74f1955c" />

```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="656" height="458" alt="image" src="https://github.com/user-attachments/assets/57cf955d-6c89-4c56-96af-3f40fe0bf730" />

```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="556" height="427" alt="image" src="https://github.com/user-attachments/assets/43d80f20-ffa9-42f2-b42f-87db9d254137" />


```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="526" height="421" alt="image" src="https://github.com/user-attachments/assets/319bf659-9d1b-4559-9980-2ca37bbe964a" />

```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="536" height="409" alt="image" src="https://github.com/user-attachments/assets/7ba2989a-d29e-4e07-8ff2-5c57fe7dbe55" />

```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="530" height="431" alt="image" src="https://github.com/user-attachments/assets/a43c88f0-55eb-4936-a004-825783e2af46" />

```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="541" height="426" alt="image" src="https://github.com/user-attachments/assets/000d222f-a578-4489-bc8c-172611a96699" />

```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="548" height="431" alt="image" src="https://github.com/user-attachments/assets/6be9e208-61ce-40a6-8c4e-ad971536587b" />

```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```


<img width="557" height="475" alt="image" src="https://github.com/user-attachments/assets/fc307ed9-28e0-4b81-bb16-a84cd7e1fa54" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
