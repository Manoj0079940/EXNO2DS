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

## CODING AND OUTPUT
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
dt=pd.read_csv("titanic_dataset.csv")
dt
![image](https://github.com/user-attachments/assets/261f54de-b6da-4c59-a904-35395ea00ec6)

## dt.info()

![image](https://github.com/user-attachments/assets/3ef85f91-16c6-4c2d-96a8-e14b3b3b1b16)

## dt.set_index("PassengerId")

![image](https://github.com/user-attachments/assets/d984353b-e3c4-4e94-a451-b7919a813722)

## dt.nunique()

![image](https://github.com/user-attachments/assets/49963f64-f176-471f-9323-fa47eb436ccf)

## dt["Survived"].value_counts()

![image](https://github.com/user-attachments/assets/31691146-bb95-44cb-87c2-6c3094a2e9dd)

## per=(dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
per

![image](https://github.com/user-attachments/assets/ecb22e55-1e85-47cb-89d4-2642ffef34d0)

## sns.countplot(data=dt,x="Survived")

![image](https://github.com/user-attachments/assets/a50e9795-d1f6-4cc1-a42f-ab196eb51448)

## dt.Pclass.unique()

![Screenshot 2024-09-03 153632](https://github.com/user-attachments/assets/e417b4c0-e980-4f40-a02a-f01b937cd554)

## dt.rename(columns={'Sex':'Gender'},inplace=True)
dt

![Screenshot 2024-09-03 153844](https://github.com/user-attachments/assets/b473dafb-983e-4e57-932d-462f9d94304f)

## sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)

![Screenshot 2024-09-03 153947](https://github.com/user-attachments/assets/2db26538-9c7b-47ef-9251-1a6cd6dfde5c)

## sns.catplot(x="Survived",hue="Gender",data=dt,kind="count")

![Screenshot 2024-09-03 154047](https://github.com/user-attachments/assets/0c187ed2-83dd-4c90-a591-d72753848d57)

## dt.boxplot(column='Age',by='Survived')

![image](https://github.com/user-attachments/assets/b00d5688-9679-496e-9b82-57cadcf3391b)

## sns.scatterplot(x=dt['Age'],y=dt["Fare"])

![image](https://github.com/user-attachments/assets/dc85ad26-f0f1-4841-becd-cd18a69424cc)

## sns.jointplot(x="Age",y="Fare",data=dt)

![image](https://github.com/user-attachments/assets/02c3c378-41fd-41b6-9618-353bc89d5cbc)

## sns.catplot(x="Gender",col="Survived",hue="Pclass",kind="count",data=dt)

![image](https://github.com/user-attachments/assets/5a85ea5e-3e0f-4cc0-8cd2-07cee9e6dbf1)

## corr=dt.corr()
sns.heatmap(corr,annot=True)

![image](https://github.com/user-attachments/assets/a0a3b2ff-ce0b-4733-bb51-6c1c4ad0f22b)

## sns.pairplot(dt)

![image](https://github.com/user-attachments/assets/3172a6ed-49ba-4d4e-bead-f70370d37b5a)
![image](https://github.com/user-attachments/assets/7a65e00c-0f7f-4bb3-8d91-baa265698975)

# RESULT
       Thus the data analysis has been implemented succesfully.
