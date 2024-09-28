# **Data Cleaning Project:** [messy_data.csv](https://github.com/user-attachments/files/17174145/messy_data.csv)
## *Project Overview*      
This project demonstrates a step-by-step approach to cleaning a messy dataset (messy_data.csv). The dataset contains inconsistencies such as missing values, duplicates, invalid formats, and noise in several columns. The goal of the project is to clean the dataset and prepare it for further analysis.   
## Files
[messy_data.csv](https://github.com/user-attachments/files/17174145/messy_data.csv): The raw dataset that needs to be cleaned.    
data_cleaning.py: Python script used to clean the dataset.     
## Technologies/Libraries Used  
``` javascript
 - Python 3
 - Jupyter
 - Pandas
 - Numpy
 - Seaborn
 - Matplotlib
 - re 
 - Scipy
 - fuzzywuzzy
 ```

To install required libraries, run:  
```bash
pip install pandas numpy matplotlib seaborn fuzzywuzzy scipy
```
## Data Quality Issues Identified:
1. Missing values in various columns.    
2. Duplicate records.     
3. Invalid email formats.
4. Irregular name formats.
5. Inconsistent date formats in the 'Join Date' column.
6. Inconsistent department names.
7. Salary values with unrealistic amounts.
# Cleaning Steps:
## 1. Basic Dataset Exploration
Check the first and last 5 rows of the dataset using `df.head()` and `df.tail()` .
Summarize the data: `df.info()` gives basic info, and `df.describe()` provides statistics for numeric columns.
## 2. Handling Missing Values
Identified columns with missing data using `df.isnull().sum()`.
Filled missing values:
Numeric columns (`'Age'`, `'Salary'`) with median.
Categorical columns (`'Name`', `'Email'`, `'Join Date'`, `'Department'`) with mode.
## 3. Removing Duplicates
Removed duplicate rows using `df.drop_duplicates()`.
## 4. Email Validation
Created a function `is_valid_Email()` to check and correct email formats using regular expressions.
##5. Name Cleaning
Cleaned the `'Name'` column by removing unwanted characters and standardizing names (title case).
## 6. Standardizing Date Formats
Standardized the `'Join Date'` column using `pd.to_datetime()`.
## 7. Correcting Department Names
Used `fuzzywuzzy` to correct inconsistent department names by matching them to a list of expected departments.
## 8. Handling Salary Noise
Visualized salary distribution using histograms and box plots.
Used winsorization to handle outliers in the `'Salary'` column.
Removed outliers based on the interquartile range (IQR).
## Visualizations:
* Salary Distribution (Before and After Cleaning)
* Box Plot of Salary (Before and After Outlier Removal)

  **salary plot(before distribution)**
![image](https://github.com/user-attachments/assets/60a48898-4787-42f1-8706-e58912612c46)
8* Updated salary plot **
![image](https://github.com/user-attachments/assets/8e374c2c-b581-4f47-b9f8-1776367511ca)

# Final Output
### After cleaning, the dataset is free from:

* Missing values.
* Invalid email and date formats.
* Duplicate records.
* Salary outliers.

  
             
## *The final cleaned dataset is stored in:* [cleaned_dataset.csv](https://github.com/user-attachments/files/17174144/cleaned_dataset.csv)
