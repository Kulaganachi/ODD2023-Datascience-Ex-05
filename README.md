# Feature_Encoding_Scaling
## Ex:05 Feature Generation
## AIM
To read the given data and perform Feature Generation process and save the data to a file.

## Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 
## ALGORITHM
### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature Generation techniques to all the feature of the data set

### STEP 4
Save the data to the file

## PROGRAM
Developed by:Kulaganachi

Register number:212221040086

### For Encoding.csv file
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```

### Data.csv
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
### BMI.csv file
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
## OUTPUT
### For encoding.csv file
#### Initial data:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/0bd82417-db1f-4c3b-84b1-44bee57e55fa)


### Unique value:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/69915688-cb7a-4776-a816-84f1aa503c40)


### Ordinal Encoder:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/8aa2e49a-1c46-4bcf-8d50-ba9d8a1d2d7d)


### Label Encoder:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/93a755c0-b05e-44d6-bdc3-437464854f13)


### Binary Encoder:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/e6022cde-6ec8-4ee6-8d7f-2c5004346855)


![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/1a4863bc-3aeb-46f6-b4d7-245bd51d7194)


## For Data.csv file
### Initial data:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/35305e43-77c8-4e9a-83b1-db139ca53996)


### Unique data:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/2c3c4b21-5002-483f-bfc3-7b48ad852534)


### Ordinal Encoder:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/0e1154d7-2672-4654-a6bf-73d2ec0a1405)


![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/6a048bf6-600b-4d03-abee-273256ed103f)


### Label Encoder:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/bd9888de-16e5-4979-b50d-57cefec4d481)


### Binary Encoder:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/b319effa-2009-4314-8613-0e4fc5547db3)


![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/016022b1-0062-444a-ba48-5c39c480bc18)


## For bmi.csv file
### Initial data:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/76deb17a-c35d-4256-9d70-c75ab32ddb06)


### Binary Encoders:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/341ed745-b4fb-4c63-81ca-fbba89e6569e)


### Dummies:
![image](https://github.com/Kulaganachi/Feature_Encoding_Scaling/assets/133641126/90d5c52e-6181-4e3c-a7d1-d90b0ea8b65a)


## RESULT:
The Feature Generation process was performed and saved the data to a file.

