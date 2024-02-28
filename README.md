# Glassdoor Data Science Jobs: Data Cleaning and Analysis

This repository documents the comprehensive data cleaning and analysis process for Glassdoor data science job listings. The aim is to prepare the dataset for insightful analysis and exploration of job market trends.

## Data Cleaning Steps:

1. **Job Title Standardization**: 
   - Applied `str.title()` function to standardize the format of job titles.
   - Extracted "Data Scientist" pattern from the job titles for consistency.
   
2. **Removing Irrelevant Columns**:
   - Eliminated the "Job Description" column as it was deemed extraneous to the analysis.

3. **Salary Estimation Refinement**:
   - Employed string manipulation techniques to extract salary ranges from the "Salary Estimate" column.
   - Converted salary ranges to numeric values by considering lower limits and multiplying by 1000.
   - Transformed salary ranges without "K" (indicating yearly salaries) to yearly estimates by adjusting for hourly rates (multiplying by 24*365).

4. **Rating Imputation**:
   - Imputed missing (-1) values in the "Rating" column with the mean rating for enhanced dataset completeness.

5. **Company Name Standardization**:
   - Segregated and standardized company names from the "Company Name" column using `str.title()` for uniformity.

6. **Location Information Extraction**:
   - Extracted city and state details from the "Location" column for geographical analysis.

7. **Size Data Formatting**:
   - Parsed size information in the "Salary to Salary" format.
   - Selected maximum range values using a dictionary for clarity.

8. **Founded Column Removal**:
   - Removed the "Founded" column as it was deemed unnecessary for the analysis.

9. **Handling Missing Values**:
   - Replaced missing (-1) values in the "Type of Ownership", "Industry", and "Sector" columns with "Unknown" for completeness.
   - Adjusted maximum values in the "Revenue" column to lakh units for consistency.

10. **Imputation using Iterative Imputer**:
    - Utilized Iterative Imputer technique to address 0 values in the "Salary Estimates" and "Revenue" columns.

## Data Analysis:

1. **Industries with Highest Salary Estimates**:
   - Identified industries offering the highest salary estimates for data scientists.

2. **Highest Paying Sectors**:
   - Determined the sector providing the highest salary estimates to data scientists.

3. **Ownership Influence on Salary Estimates**:
   - Analyzed the relationship between company ownership types and salary estimates.

4. **Impact of Company Size**:
   - Explored the effect of company size on salary estimates for data scientists.

5. **Top-Rated Cities and States**:
   - Identified cities and states with better-rated companies.

6. **Correlation Analysis**:
   - Investigated correlations between company ratings and salary estimates.

7. **Cities and States with Highest Salaries**:
   - Identified top cities and states with the highest average salaries for data scientists.

## Conclusion:
The meticulous data cleaning procedures and comprehensive data analysis have provided valuable insights into the Glassdoor data science job market. This cleaned and analyzed dataset serves as a reliable foundation for understanding job market trends, salary estimations, and company ratings for data scientists.
