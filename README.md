# EX.NO-1   DATA-PREPROCESSING...

## AIM:
To perform Data preprocessing in a data set downloaded from Kaggle.

## EQUIPMENTS REQUIRED:
Hardware – PCs.

Anaconda – Python 3.7 Installation / Google Colab /Jupyter Notebook.

## RELATED THEORETICAL CONCEPT:
## KAGGLE:

Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

## DATA PREPROCESSING:

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

## NEED OF DATA PREPROCESSING:

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set. Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.

## ALGORITHM:

### Step 1:
Importing the libraries.

### Step 2:
Importing the dataset.

### Step 3:
Taking care of missing data.

### Step 4:
Encoding categorical data.

### Step 5:
Normalizing the data.

### Step 6:
Splitting the data into test and train.

### Step 7:
End the program.

## PROGRAM:

```python

### Developed by : Anto Richard.S
### Reg.No : 212221240005
### Program to perform Data preprocessing in a data set downloaded from Kaggle.

import pandas as pd

df=pd.read_csv("/content/Churn_Modelling.csv")

df.head()

df.isnull().sum()

df.drop(["RowNumber","Age","Gender","Geography","Surname"],inplace=True,axis=1)

print(df)

x=df.iloc[:,:-1].values

y=df.iloc[:,-1].values

print(x)

print(y)

from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

df1 = pd.DataFrame(scaler.fit_transform(df))

print(df1)

from sklearn.model_selection import train_test_split

xtrain,ytrain,xtest,ytest=train_test_split(x,y,test_size=0.2,random_state=2)

print(xtrain)

print(len(xtrain))

print(xtest)

print(len(xtest))

from sklearn.preprocessing import StandardScaler

sc = StandardScaler()

df1 = sc.fit_transform(df)

print(df1)
```

## OUTPUT:

### DATASET:
![out1](https://user-images.githubusercontent.com/93427534/192864911-e3c9712b-a86d-4cf4-a813-c2a7d847e374.png)

### VALUES OF INPUT AND OUTPUT DATA ON VAR X AND Y:
![out2](https://user-images.githubusercontent.com/93427534/192864948-4088dd7b-16f3-48bb-9d56-f3960b42d134.png)

### NORMALIZING DATA:
![out3](https://user-images.githubusercontent.com/93427534/192864983-8520a323-33fc-4370-b0d5-edf5195f0817.png)

### X_TRAIN AND Y_TRAIN VALUES:
![out4](https://user-images.githubusercontent.com/93427534/192865066-e9ec4d24-734a-4eb6-8bf3-c9ac9b2904b6.png)

### X AMD Y VALUES:
![out5](https://user-images.githubusercontent.com/93427534/192865089-b32bf589-d0e9-4850-8eba-1f4b5acb7255.png)

### X_TEST AND Y_TEST VALUES:
![out6](https://user-images.githubusercontent.com/93427534/192865122-d0478440-af1f-4004-af95-91958176282d.png)

## RESULT:
Thus,the program to perform Data preprocessing in a data set downloaded from Kaggle is implemented successfully.. 
