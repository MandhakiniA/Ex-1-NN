<H3>ENTER YOUR NAME       : A.MANDHAKINI </H3>
<H3>ENTER YOUR REGISTER NO:212223100030</H3>
<H3>EX.NO:1</H3>
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
```py
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
### Dataset:
![image](https://github.com/user-attachments/assets/0ca9889c-ea47-4547-8120-6f14b7f29830)

### X Values:
![image](https://github.com/user-attachments/assets/327b577d-b74e-4427-873a-ccb0eb7be20b)

### Y Values:
![image](https://github.com/user-attachments/assets/d43d58d4-13b8-4f1c-ac95-03f454b6033f)

### Null Values:
![image](https://github.com/user-attachments/assets/f060d47d-c5ae-44fb-a691-1704919f771f)

### Duplicated Values:
![image](https://github.com/user-attachments/assets/15ffdbc2-f4cb-4f0b-aba8-e9d20fa6de58)

### Description:
![image](https://github.com/user-attachments/assets/fe518588-0917-4439-b1a6-ac4498ed75c1)

### Normalized Dataset:
![image](https://github.com/user-attachments/assets/c1ad7857-c09e-4474-92aa-7439d59588ed)

### Training Data:
![image](https://github.com/user-attachments/assets/7998941f-5081-4c7d-ab88-b2fc370d3dff)
### Testing Data:
![image](https://github.com/user-attachments/assets/6d8c0445-37b4-4ed9-af18-0bea340d1f00)



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


