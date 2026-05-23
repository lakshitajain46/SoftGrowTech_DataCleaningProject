# SoftGrowTech_DataCleaningProject
## Titanic Dataset Data Cleaning Project

### Project Overview
This project focuses on cleaning and preprocessing the Titanic dataset using Python and Pandas in Google Colab. The dataset contains missing values, duplicate records, and unnecessary columns that may affect machine learning model performance and data analysis accuracy.
The main objective of this project is to prepare a clean and structured dataset for further analysis and machine learning tasks.

## Objectives
- Understand data preprocessing techniques
- Handle missing values in datasets
- Remove duplicate records
- Drop unnecessary columns
- Prepare clean data for machine learning

## Tools & Technologies Used
- Python
- Pandas
- Google Colab

## Dataset Used
Titanic Dataset (`train.csv`)
Dataset Source:
https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

## Tasks Performed
- Loaded dataset using Pandas
- Checked dataset information
- Identified missing values
- Filled missing values using mean and mode
- Removed unnecessary columns
- Removed duplicate rows
- Saved cleaned dataset into a new CSV file

## Project Workflow
1. Import Libraries
2. Load Dataset
3. Explore Dataset
4. Handle Missing Values
5. Remove Unnecessary Columns
6. Remove Duplicate Records
7. Save Cleaned Dataset

## Sample Code

```python
import pandas as pd
url = "https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv"
df = pd.read_csv(url)
df['Age'].fillna(df['Age'].mean(), inplace=True)
df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)
df.drop(columns=['Cabin'], inplace=True)
df.drop_duplicates(inplace=True)
df.to_csv("cleaned_titanic.csv", index=False)
print("Dataset cleaned successfully!")

##Conclusion
The Titanic dataset was successfully cleaned and preprocessed. Missing values were handled, duplicate rows were removed, and unnecessary columns were dropped. The cleaned dataset is now ready for machine learning and data analysis applications.
