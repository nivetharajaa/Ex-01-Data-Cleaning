# Ex-01_DS_Data_Cleansing

# AIM

To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation

Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM

## STEP 1

Read the given Data

## STEP 2

Get the information about the data

## STEP 3

Remove the null values from the data

## STEP 4

Save the Clean data to the file

# CODE

import pandas as pd

df=pd.read_csv("/content/Loan_data.csv")

print(df)

df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])

df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])

df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])

df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())

df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())

df.head()

df.info()

df.isnull().sum()

# OUPUT

##DATA:

![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/20ed2513-41fa-4634-b208-42348abee952)


![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/4355a678-cd97-4122-b738-dd5cf2c787bf)


##NON NULL BEFORE


![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/a823649e-3a75-4469-bb28-b29818ceaee8)


##MODE

![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/8efaecc0-216e-4a33-9b41-0829913379c8)

##MEAN

![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/963b685d-887c-4edc-b48e-635932d789a7)

##MEDIAN

![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/4977f3b8-c8be-40b3-9643-c2c9024026ae)

##NON NULL AFTER

![image](https://github.com/nivetharajaa/Ex-01-Data-Cleaning/assets/120543388/77c5ae62-0342-4849-b7ff-4f446ea1f665)


##RESULT

Thus, the given data is read, cleansed and the cleansed data is saved into the file.











