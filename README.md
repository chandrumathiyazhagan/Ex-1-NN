<H3>ENTER YOUR NAME : M.CHANDRU</H3>
<H3>ENTER YOUR REGISTER NO : 212222230026</H3>
<H3>EX. NO.1</H3>
<H3>DATE : 22-08-2024</H3>

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

## IMPORT LIBRARIES:
```python
from google.colab import files
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```
## READ THE DATASET FROM DRIVE:
```python
df=pd.read_csv('neural.csv')
print(df)
```
## SPLIT THE DATASET:
```python
X=df.iloc[:, :-1].values
print(X)
Y=df.iloc[:, -1].values
print(Y)
```
## FINDING MISSING VALUES:
```python
print(df.isnull().sum())
```
## HANDLING MISSING VALUES:
```python
df.describe()
```
## CHECK FOR DUPLICATES:
```python
df.duplicated()
```
## DETECT OUTLIERS:
```python
df.describe()
```
## DROPPING STRING VALUES DATA FROM DATASET:
```python
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```
```python
data.head()
```
## NORMALIZE THE DATASET (MINMAX SCALER):
```python
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```
## SPLITTING THE DATA FOR TRAINING & TESTING:
```python
X_train ,X_test ,Y_train,Y_test=train_test_split(X,Y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```

## OUTPUT:

## DATASET:
![Screenshot 2024-08-23 214023](https://github.com/user-attachments/assets/ed7528c4-f262-4420-9ed0-737c76e6b0ca)

## SPLIT THE DATASET:
### X
![Screenshot 2024-08-23 214039](https://github.com/user-attachments/assets/670c9242-5b81-4c6d-9d51-236d5b07c915)

### Y
![Screenshot 2024-08-23 214049](https://github.com/user-attachments/assets/8aa8e8dd-9e7e-4a4f-81b3-7ebf979ee567)

## MISSING DATA:
![Screenshot 2024-08-23 214057](https://github.com/user-attachments/assets/dbe9f7c1-8cc3-4764-97e6-68f438de0107)

## DUPLICATES IDENTIFICATION:
![Screenshot 2024-08-23 214130](https://github.com/user-attachments/assets/262c7cd0-ca85-4449-be0e-156389177230)

## DESCRIBING DATASET:
![Screenshot 2024-08-23 214123](https://github.com/user-attachments/assets/4352b4bd-f06b-4222-85fb-0d037199c598)

## DETECT OUTLIERS:
![Screenshot 2024-08-23 214141](https://github.com/user-attachments/assets/3931e50a-9adf-44f5-94a3-df992b0970ec)

## NORMALIZED  DATASET:
![Screenshot 2024-08-23 214153](https://github.com/user-attachments/assets/5f87914d-d939-4086-bf86-e51e11e64bed)

## TRAINING & TESTING MODEL:
![Screenshot 2024-08-23 214203](https://github.com/user-attachments/assets/c2c50c96-1c3b-4157-ae51-743cbc3a1812)

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


