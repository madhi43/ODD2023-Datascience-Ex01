# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
```

![2023-08-26 (9)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/9df1f6cf-e554-4b7d-85cd-23e4f2f14b2b)

```
df.isnull()
```
![2023-08-26 (12)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/abe31319-224c-4a33-9668-3da7a3994edb)

```
df.isnull().sum()
```
![2023-08-26 (13)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/2a9b951a-9c51-4b98-9ba7-830b65550d2f)

```
df["aired_on"]=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
```

![2023-08-26 (15)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/721beaa3-d085-4f15-a6f5-a998efdff16d)


```
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![2023-08-26 (16)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/97b83cec-b27c-47ad-a034-649fd8b0cb99)
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df.head()
```
![2023-08-26 (18)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/d8656728-cd20-4e5a-a2a9-306a8a3218c7)
```
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![2023-08-26 (18)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/0f59e102-1fab-40a9-b737-b43bf97034af)
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![2023-08-26 (21)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/7aa0c383-dfdb-4be8-ba24-3f3903ff4420)


```
df.info()
```
![2023-08-26 (22)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/fccbd7f3-1fa4-478e-81d7-8c7e35a511c7)

```
df.head(10)
```
![2023-08-26 (24)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/d57d5ebf-06f0-42e9-b65b-c58c6b0f6538)

```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
```
![2023-08-26 (25)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/dedb6005-f0f7-46f1-816a-528358f1548b)

```
df.head(10)
```
![2023-08-26 (32)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/3911fd2e-6c1a-4ea2-a386-55a8ca016ab6)

```
df.info()
```
![2023-08-26 (33)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/d6344e6d-0e01-4f1f-801d-6cd06152f2d2)

```
df.isnull()
```
![2023-08-26 (34)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/4f1072d8-3eb5-442f-bf9f-7cd2e1fce3a5)

```
df.isnull().sum()
```
![2023-08-26 (35)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/cbfd8170-15ea-42e6-a85e-ca655b129c53)

```
df['Loan_ID']=df['Loan_ID'].fillna(df['LoanAmount'].mode()[0])
df.head()
```
![2023-08-26 (36)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/985c693a-b711-4d38-ad94-7d78bed10c1b)

```
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df.head()
```
![2023-08-26 (37)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/2e195854-4022-47e8-a9fb-77f245a23974)

```
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df.head()
```
![2023-08-26 (38)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/dc7bbfeb-057c-48ba-abaf-b233d91e2787)

```
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()
```
![2023-08-26 (39)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/b9218dbd-9dd4-4ba7-8db9-9b3a40542748)


```
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![2023-08-26 (40)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/a5b3bc47-78a8-4582-be08-4432fbc45bc9)


```
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![2023-08-26 (43)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/41ba99f8-9389-47c5-91d3-179c99bc9b03)

```
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
```
![2023-08-26 (44)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/e059cf98-851f-48df-ad27-976d8b990f08)
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![2023-08-26 (45)](https://github.com/madhi43/ODD2023-Datascience-Ex01/assets/103943383/640ffaad-efc2-4163-847d-ada3242df79d)
