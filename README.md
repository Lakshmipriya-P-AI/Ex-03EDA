# Ex-03EDA

## AIM:
To perform EDA on the given data set. 

# Explanation:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM:

# STEP 1: 
Create a new file in jupyter notebook.
# STEP 2:
Upload the given csv file.
# STEP 3:
Write codes for Data Analysis (EDA).
# STEP 4:
Plot the result in various formats.
# STEP 5: 
End the program.


# CODE:
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="Sex",data=df)
df.info()
sns.displot(df["Age"])
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
```

# OUPUT
![p1](https://user-images.githubusercontent.com/93427923/162117686-ae5cd94a-9736-4b27-9bee-3d74f079c86c.png)
![p2](https://user-images.githubusercontent.com/93427923/162117710-21e804e1-5cbd-427f-9929-fc3e2c1a9c68.png)
![p3](https://user-images.githubusercontent.com/93427923/162117741-39c2019b-617e-482f-9b02-8ee8fe93a7f3.png)
![p4](https://user-images.githubusercontent.com/93427923/162117764-fbcf630b-626c-46c0-92a1-6bcbf16540d9.png)
![p5](https://user-images.githubusercontent.com/93427923/162117783-e5b42f79-4319-4879-8635-30a888a7fca6.png)
![p6](https://user-images.githubusercontent.com/93427923/162117814-5574cf0a-e78b-450a-b52a-ea90fc828e91.png)
![p7](https://user-images.githubusercontent.com/93427923/162117832-6887be9f-e365-4465-8a98-92b1c08003b5.png)
![p8](https://user-images.githubusercontent.com/93427923/162117846-69fd3263-7b84-4767-b2e9-1facde20a60a.png)
![p9](https://user-images.githubusercontent.com/93427923/162117862-80601ef5-a51b-49a3-a59d-58f97c4701a3.png)

# RESULT:
Thus the data of the dataset is analyzed using Exploratory data analysis
