<H3>ENTER YOUR NAME</H3>
SATHYAA R

<H3>ENTER YOUR REGISTER NO.</H3>
212223100052

<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:

### Import Libraries
```
from google.colab import files
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
import numpy as np
```

### Read and print the dataset
```
df = pd.read_csv('Churn_Modelling.csv')
print(df)
```

### Checking Data
```
df.head()
df.tail()
df.columns
```

### Check the missing data
```
df.isnull().sum()
```

### Check for Duplicates
```
df.duplicated()
```

### Assigning Y
```
y = df.iloc[:, -1].values
print(y)
```

### Check for duplicates
```
df.duplicated()
```

### Check for outliers
```
df.describe()
```

### Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```

### Checking datasets after dropping string values data from dataset
```
data.head()
```

### Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```

### Split the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```

### Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```


## OUTPUT:

### Data checking

![image](https://github.com/user-attachments/assets/72c5b46d-474c-4f61-a4cb-d36edf248168)

### Missing data

![image](https://github.com/user-attachments/assets/865d9a07-619a-4e6d-8337-dbf99c1476e6)

### Duplicated

![image](https://github.com/user-attachments/assets/d41f49fa-4696-49f1-a689-86abe25b3242)


### Values of 'Y'

![image](https://github.com/user-attachments/assets/e9f40a74-3695-4589-9411-f33ea592546f)


### Outliers

![image](https://github.com/user-attachments/assets/ddcdb901-9233-4070-80e7-b7560ba289b6)
![image](https://github.com/user-attachments/assets/fce2b26d-55ec-40a7-a67a-1b40fd13bd82)


### Checking datasets after dropping string values data from dataset

![image](https://github.com/user-attachments/assets/eb0d0f56-b419-4e49-b271-d1c60364d08e)


### Normalize the dataset

![image](https://github.com/user-attachments/assets/115e3a20-39c0-49a0-be83-5365acc7c0fc)


### Split the dataset

![image](https://github.com/user-attachments/assets/62bb503d-a3c4-47ee-b87e-0c1b8bd488d1)


### Training and testing model

![image](https://github.com/user-attachments/assets/a3bb2a10-7535-4dbf-8ef5-e923025517bb)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


