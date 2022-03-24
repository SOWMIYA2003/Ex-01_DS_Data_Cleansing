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


# CODE
```
import pandas as pd
df = pd.read_csv("Data_set.csv")
df.head(10)
df.tail()
df.info()
df.isnull().sum()
df["show_name"]=df["show_name"].fillna(df["show_name"].mode()[0])
df.head(10)
df["rating"]=df["rating"].fillna(df["rating"].mean())
df.info()
df["aired_on"]=df["aired_on"].fillna(df["aired_on"].mode()[0])
df.info()
df["original_network"]=df["original_network"].fillna(df["original_network"].mode()[0])
df.info()
df["current_overall_rank"]=df["current_overall_rank"].fillna(df["current_overall_rank"].median())
df.info()
df["watchers"]=df["watchers"].fillna(df["watchers"].median())
df.info()
```
# OUPUT
### Data Frame:
![Output](./ex1a.png)
![Output](./ex1b.png)

### Columns with their corresponding Non-Null data count:
![Output](./ex1c.png)

### Sum of Null data in corresponding Columns:
![Output](./ex1d.png)

### Column- show_name:
#### Before handling Null data:
![Output](./1.png)
#### After handling Null data:
![Output](./2.png)

### Column- rating:
#### Before handling Null data:
![Output](./rating3.png)
#### After handling Null data:
![Output](./3.png)
![Output](./rating1.png)


### Column- aired_on:
#### Before handling Null data:
![Output](./airedon1.png)
#### After handling Null data:
![Output](./airedon2.png)
![Output](./airedon.png)
### Column- original_network:
#### Before handling Null data:
![Output](./on1.png)
#### After handling Null data:
![Output](./on2.png)
![Output](./originalnetwork.png)
### Column- current_overall_rank:
#### Before handling Null data:
![Output](./ow1.png)
#### After handling Null data:
![Output](./ow2.png)
![Output](./currentoverallrank.png)
### Column- watches:
#### Before handling Null data:
![op](./wt1.png)
#### After handling Null data:
![op](./wt2.png)
![Output](./watches.png)
### After Handling all Null data:
![Output](./final.png)
## Result:
Missing data Or Null data has been handled and regularly structured  data is produced. 