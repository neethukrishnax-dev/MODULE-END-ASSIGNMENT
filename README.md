DATA CLEANING 
1) Opened the dataset containing the Medical Examinations and Hospitalization Details tables.
   Checked each column in the Medical Examinations table for missing values marked with "?".
   Medical Examination > fiter check? > smoker(2-?)
   Repeated the same procedure for the Hospitalization Details table.
   Month-3, Hospital tier 1, city tier 1, state ID 1,Customer ID 6
2) Selected the missing values in the month column
   Month > Transform > Replace Value (replaced "sep" )>ok
   Checked the year column to identify missing values
   Calculated the average of the available numerical values in the year column, excluding missing values.
   Year > Transform > Statics > Average
3) Opened the dataset containing the smoker, Hospital tier and City tier columns.
   Hospital tier > Transform > Group by > ok > count > sortdecending >find amount > Hospital tier > Replace value
   Hospital tier 1338, city tier 808 (tier 2)
4) Selected the "State ID" > Checked the column for missing values marked with '?' >  Clicked Replace All to replace the missing State ID values

DATA TRANSFORMATION
1) Selected the "names" column > Transform >  Split > by delimiter > split at > left- most delimiter > Renamed the resulting columns 
2) Opened the Medical Examinations table in Power Query Editor > Selected the "NumberOfMajorSurgeries" column. > Trasform > replace > value 
   ( Changed the column data type to Whole Number) 
3) Checked the "Heart Issues" and "smoker" columns for inconsistent values 
   hear issue >  transform > capitalized each word > trim 
4) BMI >Created a new column > conditional column > apply conditional column formulas 
5) HbA1C > Add column > conditional columns > apply conditional column formula s> close & load 
6) Selected the "year", "month", and "date" columns >Add column > Merge column > Apply formate > ok> select the date of birth > transform > data type > date > close & load
7) hospitalisation > add column > custom column > table > formatte apply
    Used 8 June 2023 as the dataset collection date.
    Calculated age by considering the year, month, and day of birth.
    Set the Age column data type to Whole Number.
