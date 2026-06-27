# DSA3050A Mid-Semester Practical Examination

## Student Information
- Name: Samuel Kasusya
- Student ID: 668694

## Dataset Information
- Dataset Name: Diabetes 130-US Hospitals for Years 1999-2008
- Source: UCI Machine Learning Repository - https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008
- Number of Rows: 101,767
- Number of Columns: 47 (reduced to 29 after removing unnecessary columns and querying)
- Business Problem: This project looks at patient admissions, readmission rates, and length of stay across a US hospital network to find patterns that can help improve healthcare efficiency and reduce costly readmissions.

## Power Query Transformations Performed
1. Replaced question mark values with null across all columns
2. Removed unnecessary columns including medication columns, payer_code and weight
3. Renamed unclear columns for example admission_type_id was renamed to Admission_Type
4. Changed data types for numeric columns to Whole Number
5. Removed duplicate records based on encounter_id
6. Removed blank rows
7. Trimmed and cleaned text columns
8. Split the age column by delimiter
9. Merged race and gender into a new Patient_Demographics column
10. Created a conditional column called Stay_Category with Long Stay and Short Stay values
11. Created a custom column called Procedure_Intensity
12. Filtered rows using two conditions on readmitted and Stay_Category
13. Sorted data by Days_In_Hospital in descending order
14. Added an index column
15. Duplicated the query for aggregation analysis
16. Used Group By on race with multiple aggregations
17. Created a reference query
18. Extracted text before a delimiter from the diag_1 column
19. Used column profiling to identify data quality issues

## Visuals Created
1. KPI Card - Total Patients
2. KPI Card - Total Readmissions
3. KPI Card - Average Days in Hospital
4. Bar Chart - Patients by Race
5. Line Chart - Average Diagnoses by Race
6. Donut Chart - Readmission Distribution
7. Table - Patient Records
8. Matrix - Patient Stay Category by Race
9. Stacked Bar - Average Stay by Gender and Stay Category
10. Clustered Bar - Average Lab Procedures by Race
11. Column Chart - Patients by Stay Category
12. Slicers - Race, Gender, Readmitted

## Business Insights
1. Caucasian patients make up the largest share of hospital admissions across all racial groups. This could reflect the demographic makeup of the hospitals studied but it also raises questions about whether minority groups are getting equal access to diabetes care.

2. About 75.79% of readmitted patients came back after 30 days while 24.21% were readmitted within 30 days. Patients who return within 30 days are a concern because it often means the first treatment did not go well and these cases tend to be more expensive to manage.

3. The average hospital stay is 4.56 days. Patients who stay longer than 7 days are fewer in number but they likely use a much larger share of hospital resources. Looking into what drives long stays could help the hospital plan better and reduce costs.

## Notes
- The dataset did not contain geographic location data so a map visual was not included.
- The dataset did not have a full date column so date based transformations were not performed.
