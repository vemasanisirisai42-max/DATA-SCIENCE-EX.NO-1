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
import pandas as pd

# Read the dataset
data = pd.read_csv("C:/Users/acer/Downloads/Data_set (1).csv")

# Convert into DataFrame
df = pd.DataFrame(data)

# Fill missing values using forward fill method
dfd = df.fillna(method="ffill")

# Display output
print("AFTER FILLNA")

print(dfd)
```

<img width="698" height="671" alt="image" src="https://github.com/user-attachments/assets/2a8c1655-8104-44f0-9ead-0c02d3331792" />

```
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Read the dataset
data = pd.read_csv("C:/Users/acer/Downloads/iris.csv")

# Convert into DataFrame
df = pd.DataFrame(data)

# Display dataset
print(df)

# Select columns
x = df["petal_length"]
y = df["sepal_length"]

# Create histogram
plt.hist(x)

# Display graph
plt.show()

# Create another histogram
plt.hist(y)

# Display graph
plt.show()
```

<img width="565" height="882" alt="image" src="https://github.com/user-attachments/assets/288267a3-86a5-48f0-9230-f4bddf9fa28a" />

```
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Read dataset
data = pd.read_csv("iris.csv")

# Convert into DataFrame
df = pd.DataFrame(data)

# Display dataset
print(df)

# Select columns
x = df["petal_length"]
y = df["sepal_length"]

# Label axes
plt.xlabel('X-axis')
plt.ylabel('Y-axis')

# Plot graph
plt.plot(x, y)

# Display graph
plt.show()
```

<img width="604" height="580" alt="image" src="https://github.com/user-attachments/assets/d7f34551-63ca-4dec-a2e3-46d691ff0bac" />

```
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Read dataset
data = pd.read_csv("iris.csv")

# Convert into DataFrame
df = pd.DataFrame(data)

# Display dataset
print(df)

# Create boxplot
dff = plt.boxplot(df["petal_width"])

# Display graph
plt.show()

print(dff)
```

<img width="916" height="643" alt="image" src="https://github.com/user-attachments/assets/a92cd39d-4c24-4b2e-aa39-a63a3809dc7f" />

```
\import pandas as pd
import numpy as np
from scipy import stats

data = pd.read_csv("iris.csv")

df = pd.DataFrame(data)

z_scores = np.abs(stats.zscore(df.select_dtypes(include=[np.number])))

df_cleaned = df[(z_scores < 3).all(axis=1)]

print(df_cleaned)
```

<img width="608" height="217" alt="image" src="https://github.com/user-attachments/assets/a39e373a-7ebf-494c-8277-f4e73ffa823a" />


```
import pandas as pd
import numpy as np

data = pd.read_csv("C:/Users/acer/Downloads/iris (1).csv")
df = pd.DataFrame(data)

Q1 = df["sepal_width"].quantile(0.25)

Q3 = df["sepal_width"].quantile(0.75)

IQR = Q3 - Q1

lower_bound = Q1 - 1.5 * IQR

upper_bound = Q3 + 1.5 * IQR

print("The Original DataSet")

print(df)

outliers = df[
    (df['sepal_width'] < lower_bound) |
    (df['sepal_width'] > upper_bound)
]

print("The Outliers")

print(outliers)

df_clean = df[
    (df['sepal_width'] >= lower_bound) &
    (df['sepal_width'] <= upper_bound)
]

print("The Dataset after removing the outliers")

print(df_clean)
```

<img width="605" height="521" alt="image" src="https://github.com/user-attachments/assets/82cc528f-f488-4a40-b668-53ca733a4e85" />

# Result

THUS DATA CLEANING IS PERFORMED
         
