# EXNO2DS
# AIM:
To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv('/content/titanic_dataset.csv')
print(df)
df.info()
df.shape
df.nunique()
df["Survived"].value_counts()
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
print(per)

sns.countplot(data=df,x="Survived")

df.set_index("PassengerId",inplace=True)

df.describe()
df.Pclass.unique()
print(df)

sns.catplot(x="Sex",col="Survived",kind="count",data=df,height=5,aspect=.7)

sns.catplot(x='Survived',hue="Sex",data=df,kind="count")

df.boxplot(column="Age",by="Survived")

sns.scatterplot(c=df["Age"],y=df["Fare"])

sns.jointplot(x="Age",y="Fare",data=df)

fig,ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=df)

sns.catplot(data=df,col="Survived",x="Sex",hue="Pclass",kind="count")

sns.pairplot(df)

numeric=df.select_dtypes(include=['number'])
corr=numeric.corr()
sns.heatmap(corr,annot=True)
```

![image](https://github.com/user-attachments/assets/e8b6a90b-384e-4e57-94a6-1baf7b2f0649)

![image](https://github.com/user-attachments/assets/bb2b5e36-4de8-46a4-b4c9-00cfc2416a78)

![image](https://github.com/user-attachments/assets/d89ef2a8-797a-443d-9983-271141e4d417)

![image](https://github.com/user-attachments/assets/12b786e7-6ea6-480e-9480-532c5b514bf1)

![image](https://github.com/user-attachments/assets/63709258-0baf-4a53-afcf-0fee60c338f8)

![image](https://github.com/user-attachments/assets/3513e47e-2576-418c-b7ba-b4ac39678d77)

![image](https://github.com/user-attachments/assets/c9fd24c9-1d53-4cc4-8f9b-ae5d1bcd45c6)

![image](https://github.com/user-attachments/assets/fbd968f9-f10a-4b98-9357-775640a03186)

![image](https://github.com/user-attachments/assets/88c13c3b-e77e-478a-9dce-bbf8f0e34c3b)

![image](https://github.com/user-attachments/assets/33be2204-f890-4738-9e8b-0ff7167f2e21)

![image](https://github.com/user-attachments/assets/47e08e7e-af21-4378-b263-3c194539a629)

![image](https://github.com/user-attachments/assets/ee955bb2-2912-4c51-845b-35a8524a2dd1)

![image](https://github.com/user-attachments/assets/9f6f2ca1-66ca-4461-8c09-0189eec722a1)




# RESULT:
Thus the code has been executed successfully.

