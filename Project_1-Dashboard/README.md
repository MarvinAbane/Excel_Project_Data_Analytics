# Excel Salary Dashboard  

<img width="1440" height="683" alt="1_Salary_Dashboard" src="https://github.com/user-attachments/assets/4e564c27-178b-443a-8237-854ce7580c1d" />  

## Introduction  

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  
The data is from my Excel course by @lukebarousse, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.  

## Dashboard file  
[Click here for my final Dashboard](1_Salary_Dashboard.xlsx)  

## Excel Skills Used  

The following Excel Skills were utilized for the analysis.  

📉 Charts  
🧮 Formulas and Functions  
❎ Data Validation    

## Data jobs dataset  

The dataset used for this project contains real-world data science job information from 2023.   

👨‍💼 Job titles  
💰 Salaries  
📍 Locations  
🛠️ Skills    

## Dashboard build  

### Charts  

#### 📊 Data Science Job Salaries - Bar Chart  

<img width="533" height="311" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/dc4c6d9e-4efc-4d9a-af28-b60b8d1c0da8" />  

🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.  
🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.  
📉 Data Organization: Sorted job titles by descending salary for improved readability.  
💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.  

#### 🗺️ Country Median Salaries - Map Chart  

<img width="439" height="297" alt="1_Salary_Dashboard_Chart2" src="https://github.com/user-attachments/assets/e42f3449-bafb-438e-b1e6-fcb90b0263e8" />  

🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.  
🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.  
📊 Data Representation: Plotted median salary for each country with available data.  
👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.  
💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.  

### Formulas and Functions  

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.  
📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.  
🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.  
🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.  

🍽️ Background Table  

<img width="205" height="164" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/e964eb1c-ea47-4f60-897a-4cc98375f903" />  

📉 Dashboard Implementation  

<img width="449" height="538" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/72018bc4-8396-48f6-be0c-769395fb7207" />  

⏰ Count of Job Schedule Type  

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.  
🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.  

🍽️ Background Table  

<img width="204" height="92" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/fcdd1d97-52e9-4865-a904-5d3c231b52c1" />  

📉 Dashboard Implementation:  

<img width="449" height="538" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/8c2e2c96-5f96-45c6-bc1b-993571167b00" />  

### ❎ Data Validation  

🔍 Filtered List  
🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:  
🎯 User input is restricted to predefined, validated schedule types.  
🚫 Incorrect or inconsistent entries are prevented.  
👥 Overall usability of the dashboard is enhanced.  


## Conclusion  

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.  










