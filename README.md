<H3>ENTER YOUR NAME: V MYTHILI</H3>
<H3>ENTER YOUR REGISTER NO: 212223040123.</H3>
<H3>EX. NO.1</H3>
<H3>DATE: 25.08.24</H3>
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

```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

df=pd.read_csv('Churn_Modelling.csv')
print(df)
```

```

df.head(6)


```

```
x = df.iloc[:, :-1].values
print(x)
```


```

y = df.iloc[:, -1].values
print(y)

```

```
df.isnull()

```

```

print(df.isnull().sum())

```

```

df.duplicated()

```


```

df.describe()

```


```

print(df['Gender'].describe())

```

```

df=pd.read_csv('Churn_Modelling.csv')
df = df.drop(['Surname', 'Geography', 'Gender'], axis=1)
df.head()

```

```

scaler = MinMaxScaler()
df1 = pd.DataFrame(scaler.fit_transform(df))
print(df1)

```

```

import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
df=pd.read_csv('Churn_Modelling.csv')
scaler = MinMaxScaler()
x_train, x_test, y_train, y_test = train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_test))
print(x_test)
print(len(x_test))

```


## OUTPUT:







NORMALISED SET:



![image](https://github.com/user-attachments/assets/1007e302-911c-4311-9fd9-5ed3bfe0cf98)


HEAD (6):



![image](https://github.com/user-attachments/assets/3c1282b0-5e9a-4895-b200-9eeb73675c97)



X VALUES: 


![image](https://github.com/user-attachments/assets/c7e473e3-19d5-4bbf-9d8a-4639e84b42c5)


Y VALUES:

![image](https://github.com/user-attachments/assets/df961348-99f7-423f-ba1a-374040643fd9)


NULL VALUES:

![image](https://github.com/user-attachments/assets/fcae19a5-aafd-4c2a-beea-204260dd2626)



DUPLICATED VALUES:


![image](https://github.com/user-attachments/assets/806b9f35-91c6-4a93-941e-b5f0606e25b4)


DESCRIBED VALUES:

![image](https://github.com/user-attachments/assets/b0d726c7-7143-4257-abcf-f0f9261f2e73)


DROP VALUE:



![image](https://github.com/user-attachments/assets/fdab990d-06b5-4360-8d82-353ae0b1abdf)



TRAINING DATA AND TESTING DATA:

![image](https://github.com/user-attachments/assets/044a771f-12b3-46c9-b513-247be438ac3d)



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


