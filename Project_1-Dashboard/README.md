# Excel Salary Dashboard

<img width="800" height="333" alt="1_Salary_Dashboard_Final_Dashboard" src="https://github.com/user-attachments/assets/7dbece84-f330-4576-9d04-4df10fc729ec" />



##
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

### Dashboard File
My Final dashboard is in [1_Salary_Dashboard.xlsx](https://github.com/willbardon/Excel_Project-Data_Analytics/blob/main/Project_1-Dashboard/Data%20Science%20Salary%20Calculator.xlsx)

### Excel Skills Used
I applied the following skills:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation



### Data Jobs Dataset
The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills


## Dashboard Build
## 📉  Charts
-📊 **Data Science Job Salaries - Bar Chart**
![Salary Dashboard Chart 1](https://github.com/user-attachments/assets/8dcdf72e-a12d-4b30-a7b8-c12dab687979)

- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

🗺️ **Country Median Salaries - Map Chart**
<img width="800" height="430" alt="1_Salary_Dashboard_Country_Map" src="https://github.com/user-attachments/assets/37885774-9373-4b74-9fbe-59dd480af7df" />


- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

## 🧮 Formulas and Functions
💰 **Median Salary by Job Titles**
```excel
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
- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- 🔢 **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

<img width="265" height="220" alt="image" src="https://github.com/user-attachments/assets/3433ad39-bc51-4076-82cb-2c350d33dff7" /> 




📉 Dashboard Implementation
<img width="1148" height="1214" alt="image" src="https://github.com/user-attachments/assets/fbbe0433-05a5-49ee-a879-757888f09bcc" /> 


⏰ Count of Job Schedule Type
```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
- 🔍 **Unique List Generation:** This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 **Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

<img width="195" height="119" alt="image" src="https://github.com/user-attachments/assets/ea811ffb-52e6-4839-ab40-9be5b585b01f" /> 



📉 Dashboard Implementation:


- ❎ Data Validation
- 🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
- 🎯 User input is restricted to predefined, validated schedule types
- 🚫 Incorrect or inconsistent entries are prevented
- 👥 Overall usability of the dashboard is enhanced

<img width="624" height="602" alt="1_Salary_Dashboard_Data_Validation" src="https://github.com/user-attachments/assets/fae58838-bb81-4562-82a6-b589a1ad6855" />


## Conclusion
I created this dashboard to showcase insights into salary trends across various data-related job titles. Using publicly available jobs data, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
