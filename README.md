<H3>ENTER YOUR NAME</H3> M. R. ANUMITHA
<H3>ENTER YOUR REGISTER NO.</H3> 212223040018
<H3>EX. NO.1</H3>
<H3>DATE</H3> 26-08-2025
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
TYPE YOUR CODE HERE
```
``
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

data = pd.read_csv("Churn_Modelling.csv")
data
data.head()

X=data.iloc[:,:-1].values
X

y=data.iloc[:,-1].values
y

data.isnull().sum()

data.duplicated()

data.describe()

data = data.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()

scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)

X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)

X_train

X_test

print("Lenght of X_test ",len(X_test))

```

## OUTPUT:
SHOW YOUR OUTPUT HERE

Dataset:

<img width="1035" height="347" alt="Screenshot 2025-08-26 081830" src="https://github.com/user-attachments/assets/69c6bd56-b4c6-4180-b953-9920e853c96a" />

X Values:

<img width="895" height="310" alt="Screenshot 2025-08-26 081844" src="https://github.com/user-attachments/assets/9bcd282c-e2ae-4113-a4be-c55db6ec3e28" />

Y Values:

<img width="403" height="145" alt="Screenshot 2025-08-26 081859" src="https://github.com/user-attachments/assets/7d3a01bc-9aba-4504-87f0-74e3a3553865" />

Null Values:

<img width="283" height="665" alt="Screenshot 2025-08-26 081909" src="https://github.com/user-attachments/assets/f48ca474-bc44-43d8-af4d-047f66f4707c" />

Duplicated Values:

<img width="291" height="714" alt="Screenshot 2025-08-26 081919" src="https://github.com/user-attachments/assets/f7864dab-ebf2-4f7d-8fba-942d19dab518" />

Description:

<img width="1026" height="229" alt="Screenshot 2025-08-26 081928" src="https://github.com/user-attachments/assets/3b16b2c9-5d5b-40f4-923a-7f4f8c4e82d1" />

Normalized Dataset:

<img width="915" height="742" alt="Screenshot 2025-08-26 082003" src="https://github.com/user-attachments/assets/f0b0fcba-1518-4040-8cc3-4bafadb4f3be" />

Training Data:
<img width="877" height="223" alt="Screenshot 2025-08-26 082014" src="https://github.com/user-attachments/assets/5a5c6865-84f2-42d1-b537-735b436f3b13" />

Testing Data:

<img width="862" height="209" alt="Screenshot 2025-08-26 082021" src="https://github.com/user-attachments/assets/cce8e03f-4377-43a0-9f11-3e33c684f858" />
<img width="869" height="82" alt="Screenshot 2025-08-26 082027" src="https://github.com/user-attachments/assets/109aad71-b33c-4f1e-a68a-8a90a4f5d17f" />


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


