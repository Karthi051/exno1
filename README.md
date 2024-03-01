# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(5)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'])
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
# output
# display
![image](https://github.com/Karthi051/exno1/assets/148327224/373a3ba2-437f-4452-b4c7-db185754a20b)
# head
![image](https://github.com/Karthi051/exno1/assets/148327224/a609587f-f732-4a93-9d24-baad205899bf)
# tail
![image](https://github.com/Karthi051/exno1/assets/148327224/1c153bb2-a753-4e2f-9478-ec709760b566)
# info
![image](https://github.com/Karthi051/exno1/assets/148327224/31c5ae58-e981-48c6-803e-be21ca24125f)
# isnull
![image](https://github.com/Karthi051/exno1/assets/148327224/a3514903-3fd7-45b8-b0d5-7c843d6456ce)
# isnull sum
![image](https://github.com/Karthi051/exno1/assets/148327224/ea595f51-d2a7-4681-b139-713e958370f7)
# rating mean
![image](https://github.com/Karthi051/exno1/assets/148327224/400253af-c445-4ff5-a7d4-f34888a670a0)
# dropna
![image](https://github.com/Karthi051/exno1/assets/148327224/977ec813-37b4-46d2-92fb-7804f787b338)
# fillna
![image](https://github.com/Karthi051/exno1/assets/148327224/186ddaf8-e843-46f2-bc42-2ea765ed3271)









# Result
the data cleaning process has been done successfully
