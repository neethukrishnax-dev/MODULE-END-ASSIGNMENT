DATA CLEANING 
1) Checked each column in the Medical Examinations table for missing values marked with "?". >  Medical Examination > fiter check? > smoker(2-?)
   Repeated the same procedure for the Hospitalization Details table. >  Month-3, Hospital tier 1, city tier 1, state ID 1,Customer ID 6
2) Selected the missing values in the month column >  Month > Transform > Replace Value (replaced "sep" )>ok >  Checked the year column to identify missing values
   Calculated the average of the available numerical values in the year column, excluding missing values. > Year > Transform > Statics > Average
3) Opened the dataset containing the smoker, Hospital tier and City tier columns. >  Hospital tier > Transform > Group by > ok > count > sortdecending >find amount    > Hospital tier > Replace value >  Hospital tier 1338, city tier 808 (tier 2)
4) Selected the "State ID" > Checked the column for missing values marked with '?' >  Clicked Replace All to replace the missing State ID values
DATA TRANSFORMATION
1) Selected the "names" column > Transform >  Split > by delimiter > split at > left- most delimiter > Renamed the resulting columns 
2) Opened the Medical Examinations table in Power Query Editor > Selected the "NumberOfMajorSurgeries" column. > Trasform > replace > value 
   ( Changed the column data type to Whole Number) 
3) Checked the "Heart Issues" and "smoker" columns for inconsistent values > hear issue >  transform > capitalized each word > trim 
4) BMI >Created a new column > conditional column > apply conditional column formulas 
5) HbA1C > Add column > conditional columns > apply conditional column formula s> close & load 
6) Selected the "year", "month", and "date" columns >Add column > Merge column > Apply formate > ok> select the date of birth > transform > data type > date >close    & load
7)  hospitalisation > add column > custom column > table > formatte apply >  Used 8 June 2023 as the dataset collection date. >Calculated age by considering the         year, month, and day of birth. >   Set the Age column data type to Whole Number.
8) Charges > Transform > Data type > Currency > select the charges column > ctrl+1 > $ > ok
 Data Exploration, Analysis & Visualization
* Create "Health Care" sheet.> Columns Created >Formulas Used =VLOOKUP($A2,'Customer Names (2)'!$A:$D,3,FALSE) 
 Analysis using Pie/Donut Chart:
*Created a PivotTable to analyze total major surgeries based on transplant status (Yes/No) > Calculated the total number of major surgeries for each transplant category > Created two Dounut Charts to visualize the results > Total Major Surgeries by Transplant Status > Average HbA1C by Transplant Status
Analysis using Column/Bar Chart:
* Created a PivotTable to analyze average healthcare charges > Grouped the data by Weight Status and Diabetes Status
- Created a Clustered Column Chart to visualize the average healthcare charges> Added data labels and  chart title
- Created a PivotTable to analyze average healthcare charges across different hospital tiers and states - Grouped the data by Hospital Tier and State ID
   Changed the Charges calculation from Sum to Average>  Created a Clustered Column Chart to visualize the average healthcare charges
Analysis using Line/Scatter Plot:
*1. Opened the healthcare dataset in Microsoft Excel > Created a new worksheet named Scatter Analysis >  Selected the Age column from the healthcare dataset
    Copied the Age values and pasted them into the new worksheet using Paste Special >Values to avoid reference errors >  Selected and copied the BMI column and       pasted its values into the worksheet > Selected both Age and BMI columns > Created a Scatter Plot using Insert > Added the chart title Age vs BMI >  Copied      the Age and HbA1C columns into the same worksheet using Paste Special >  Values > Selected both columns and created another Scatter Plot > Added the chart        title Age vs HbA1C > Copied the Age and Charges columns into the worksheet using Paste Special >  Values > Copied the Age and Charges columns into the            worksheet using Paste Special  > Values  > Selected both columns and created the third Scatter Plot >  Added the chart title Age vs Healthcare Charges
 Dashboard Creation: 
  Created a separate worksheet named "Dashboard"> Added all the analysis charts to the Dashboard > 
  .Arranged the charts for better readability and visual presentation > Inserted slicers for (Weight Status,Diabetes Status)
  




  

    
  
