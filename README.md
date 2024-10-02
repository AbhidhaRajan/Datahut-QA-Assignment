# Datahut-QA-Assignment: Data Cleaning Process

## Introduction
This repository contains the data cleaning process for the Datahut QA Assignment. The goal of this task was to clean a provided dataset to ensure it was ready for analysis. The dataset included employee information such as IDs, names, ages, emails, join dates, salaries, and departments. The cleaning process focused on handling missing values, removing duplicates, correcting email formats, and standardizing the data across different fields.

## Assumptions
1. **Handling Missing Values**: 
   - For numeric fields like Age and Salary, missing values were replaced using the median or bfill of the respective column.
   - For categorical fields such as Name and Department, missing values were replaced with the mode (most frequent value) or a placeholder.
   
2. **Email Formats**: 
   - Professional emails follow the format `username@domain.com`. Malformed emails were corrected and any non-professional emails (such as `@gmail.com`, `@yahoo.com`) were removed.

3. **Age Range**: 
   - The valid working age range was assumed to be between 18 and 65 years. Any age values outside this range were capped or replaced with the median.

4. **Date Standardization**: 
   - The 'Join Date' column was standardized to the format `YYYY-MM-DD` for consistency.

## Data Cleaning Steps
1. **Loading and Inspecting the Data**:
   - The dataset was loaded into a Jupyter notebook using the pandas library for exploration and cleaning.
   
2. **Handling Missing Values**:
   - Missing values in the Age and Salary columns were filled using the median, ensuring no important numerical data was lost.
   - Categorical columns (e.g., Name, Department) had missing values filled with the most frequent value or a placeholder.

3. **Removing Duplicates**:
   - Duplicate entries were identified and removed to ensure each record in the dataset was unique.

4. **Correcting Email Formats**:
   - Malformed email addresses were corrected by inserting missing components (such as `@` and valid domains). Non-professional email addresses (e.g., `@gmail.com`, `@yahoo.com`) were filtered out to retain only professional emails.

5. **Cleaning Name Fields**:
   - Non-alphabetic characters were removed from the Name column to ensure consistency in name formatting.

6. **Standardizing Join Date**:
   - The Join Date column was converted into a standard date format (`YYYY-MM-DD`) to ensure consistency across all entries.

7. **Handling Salary Noise**:
   - Outliers in the Salary column were handled using the Interquartile Range (IQR) method to remove unrealistic salary values and maintain a reasonable range.

## Conclusion
The dataset has been thoroughly cleaned and is now ready for further analysis. All fields have been standardized, missing values have been addressed, and invalid data entries have been corrected or removed. The cleaned dataset provides reliable and consistent information, free of duplicates and invalid formats.

## Usage
To view the full code and cleaning process, please refer to the Jupyter notebook included in this repository. The cleaned dataset is saved as `cleaned_dataset.csv`.

## Contact
If you have any questions regarding the data cleaning process, feel free to reach out.
