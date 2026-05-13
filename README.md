#EX.NO:1
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
     df=pd.read_csv('D:Data_set (1).csv')
     print(df)
     print(data)
```
<img width="609" height="661" alt="image" src="https://github.com/user-attachments/assets/6733c7cc-81bb-4700-a842-1323abe8b2d8" />

```
df.describe()
```

<img width="609" height="236" alt="image" src="https://github.com/user-attachments/assets/cbf4f1cb-e026-4c4e-a87e-868204ba7cda" />

```
df=pd.DataFrame(df)
print(df.isnull())
```

<img width="672" height="449" alt="image" src="https://github.com/user-attachments/assets/da53dcea-8590-4184-8fe4-4df73d96477d" />

```
import pandas as pd
data = pd.read_csv("C:/Users/acer/Downloads/Data_set (1).csv")
df = pd.DataFrame(data)
dfd = df.dropna()
print("AFTER DROPNA")
print(dfd)
```

<img width="702" height="674" alt="image" src="https://github.com/user-attachments/assets/a95bfb3b-c33f-4d42-8274-54639f027f28" />

```
dfd = df.dropna(axis=1)

print("AFTER DROPNA")
print(dfd)
```

<img width="471" height="254" alt="image" src="https://github.com/user-attachments/assets/b1362da2-f70f-4445-9f33-3b9fb8bf3f58" />

```
dfd=df.dropna(axis=1,inplace=True)
```

<img width="635" height="59" alt="image" src="https://github.com/user-attachments/assets/190597ac-f545-4e6c-88af-f5766dc1e90c" />

```
print("AFTER DROPNA") dfd=df.dropna(axis=0)

print("AFTER DROPNA")

print(dfd)
```

<img width="806" height="397" alt="image" src="https://github.com/user-attachments/assets/c159e5f7-a818-4ab7-8bb0-11725b04da7f" />

<img width="426" height="264" alt="image" src="https://github.com/user-attachments/assets/48b5e4e7-0a22-47aa-bc09-da382857da31" />

```












# Result
          <<include your Result here>>
