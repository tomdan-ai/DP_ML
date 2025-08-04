
---

**EXERCISE 4.0**  
**Data Pre-processing: Cleaning and Preparation**  

**Aim:** To learn how to prepare raw datasets by handling missing values, detecting and managing outliers, converting data types, and performing advanced data cleaning to ensure consistency and quality before analysis or modeling.  

**Prerequisite:**  
- Jupyter Notebook/Google Colab/Visual Studio Code (with Jupyter Notebook Extension)  
- Smart Phones Dataset  
- Dependencies: NumPy, Pandas, Matplotlib, and Seaborn  

---

### **(A). DATASET OVERVIEW**  

1. What are the `Test_Date`, `Device_Name`, `Brand`, `Category`, `Price_USD`, and `User_Satisfaction_Rating` for the first 4 samples in the dataset?  
2. What are the `Test_Date`, `Device_Name`, `Brand`, `Category`, `Price_USD`, and `User_Satisfaction_Rating` for the last 4 samples in the dataset?  
3. What are the `Test_Date`, `Device_Name`, `Brand`, `Category`, `Price_USD`, and `User_Satisfaction_Rating` for 4 randomly selected samples, using your registration number as the random state?  
4. Standardize all column names to have lowercase characters and replace spaces and dashes with underscores. Provide the code used for standardization. What is the total number of samples, columns, and memory usage of the dataset?  
5. What is the total number of `float64`, `int64`, and `object` columns in the dataset?  
6. What single command can you use to produce a summary of all categorical variables in the dataset?  
7. Provide the total number of samples (count), number of unique values, top value, and frequency for the following columns: `Test_Date`, `Device_Name`, `Brand`, `Model`, `Category`, `Water_Resistance_Rating`, `Connectivity_Features`, and `App_Ecosystem_Support`.  
8. List all unique categories in the `Category` column and their total counts.  
9. List all unique brands in the `Brand` column and their total counts.  

---

### **(B). DESCRIPTIVE STATISTICS**  

10. What is the mean of all numerical features (`Price_USD`, `Descriptive Statistics`, `Descriptive Statistics`, `Step_Count_Accuracy_Percent`, `Sleep_Tracking_Accuracy_Percent`, `GPS_Accuracy_Meters`, `Health_Sensors_Count`, `Performance_Score`)?  
11. What is the standard deviation of all numerical features in the dataset?  
12. What is the minimum value of all numerical features in the dataset?  
13. What is the maximum value of all numerical features in the dataset?  
14. What is the median value of `Price_USD` across all samples?  
15. What are the 25th and 75th percentiles of `Battery_Life_Hours` in the dataset?  
16. What are the count, mean, standard deviation, minimum, and maximum of `Heart_Rate_Accuracy_Percent`?  
17. What are the count, mean, standard deviation, minimum, and maximum of `Step_Count_Accuracy_Percent`?  
18. What are the count, mean, standard deviation, minimum, and maximum of `Sleep_Tracking_Accuracy_Percent`?  
19. What are the count, mean, standard deviation, minimum, and maximum of `Performance_Score`?  

---

### **(C). CATEGORICAL FEATURE ANALYSIS**  

20. How many unique devices are listed in the `Device_Name` column?  
21. How many unique models are listed in the `Model` column?  
22. What is the most frequent `Water_Resistance_Rating` and its frequency?  
23. What is the most frequent `Connectivity_Features` value and its frequency?  
24. What is the most frequent `App_Ecosystem_Support` value and its frequency?  
25. How many devices have `Smartwatch` as their `Category`?  

26. How many devices are from the **Fitbit** brand?  
27. How many devices support **WIFI, Bluetooth, NFC, LTE** in the `Connectivity_Features` column?  
28. List all devices with **Cross-platform support** in the `App_Ecosystem_Support` column.  
29. What is the distribution of devices across the `Test_Date` values (count of devices per date)?  

---

### **(D). MISSING VALUES**  

30. Which columns in the dataset contain missing values, and how many missing values are in each?  
31. What is the total number of missing values in the `GPS_Accuracy_Meters` column?  
32. What percentage of values are missing in the `GPS_Accuracy_Meters` column?  
33. Using a **heatmap**, visualize missing values in the columns: `Device_Name`, `Brand`, `Model`, `Category`, `Water_Resistance_Rating`, `Connectivity_Features`, and `App_Ecosystem_Support`. Provide the code used.  
34. Using **pandas**, create a bar chart of missing values per column in the dataset. Provide the code and comment on the observations.  
35. Using the **missingno** library, visualize the missing data pattern in the dataset. Provide the code and comment on the output.  
36. Suggest an approach for replacing missing values in the `GPS_Accuracy_Meters` column, and justify why this approach is appropriate.  
37. Replace missing values in the `GPS_Accuracy_Meters` column with the **median** value. Provide the code used.  
38. Suggest an approach for replacing missing values in the `User_Satisfaction_Rating` column, if any, and justify your choice.  
39. After replacing missing values in `GPS_Accuracy_Meters`, verify that there are no missing values left in this column. Provide the code used.  

---

### **(E). OUTLIER DETECTION AND HANDLING**  

40. Using the **IQR method**, identify outliers in the `Price_USD` column. List the outlier values.  
41. Using the **IQR method**, identify outliers in the `Battery_Life_Hours` column. List the outlier values.  
42. Using the **IQR method**, identify outliers in the `Heart_Rate_Accuracy_Percent` column. List the outlier values.  
43. Using the **IQR method**, identify outliers in the `Step_Count_Accuracy_Percent` column. List the outlier values.  
44. Using the **IQR method**, identify outliers in the `Sleep_Tracking_Accuracy_Percent` column. List the outlier values.  
45. Using the **IQR method**, identify outliers in the `Performance_Score` column. List the outlier values.  
46. Provide the code to **remove outliers** from all numerical columns using the IQR method.  
47. What is the **sample size** of the dataset after removing outliers from all numerical columns?  
48. Create **box plots** for all numerical columns **before** removing outliers. Provide the code used.  
49. Create **box plots** for all numerical columns **after** removing outliers. Provide the code used and comment on the differences.  

---

### **(F). VISUALIZATION**  

50. Create a **histogram** for `Price_USD` with **50 bins** and a **KDE curve**. Provide the code used.  
51. Create a **histogram** for `Battery_Life_Hours` with **50 bins** and a **KDE curve**. Provide the code used.  
52. Create a **histogram** for `Heart_Rate_Accuracy_Percent` with **50 bins** and a **KDE curve**. Provide the code used.  
53. Create a **histogram** for `Step_Count_Accuracy_Percent` with **50 bins** and a **KDE curve**. Provide the code used.  
54. Create a **histogram** for `Sleep_Tracking_Accuracy_Percent` with **50 bins** and a **KDE curve**. Provide the code used.  
55. Create a **bar plot** showing the **average** `User_Satisfaction_Rating` by `Category`. Provide the code used.  
56. Create a **bar plot** showing the **average** `Performance_Score` by `Brand`. Provide the code used.  
57. Create a **box plot** showing the distribution of `Price_USD` by `Category`. Provide the code used.  
58. Create a **box plot** showing the distribution of `Battery_Life_Hours` by `Brand`. Provide the code used.  
59. Create a **scatter plot** of `Heart_Rate_Accuracy_Percent` vs. `Step_Count_Accuracy_Percent`, colored by `Category`. Provide the code used.  


### **(G). CORRELATION ANALYSIS**  

60. Create a **lower triangle correlation heatmap** for numerical columns. Provide the code used.  
61. What is the correlation coefficient between `Heart_Rate_Accuracy_Percent` and `Step_Count_Accuracy_Percent`?  
62. What is the correlation coefficient between `Price_USD` and `Performance_Score`?  
63. What is the correlation coefficient between `Battery_Life_Hours` and `User_Satisfaction_Rating`?  
64. Create a **pairplot** for numerical columns (`Price_USD`, `Battery_Life_Hours`, `Heart_Rate_Accuracy_Percent`, `Step_Count_Accuracy_Percent`, `Performance_Score`), colored by `Category`. Provide the code used.  
65. Which numerical features have the **highest positive correlation** with `Performance_Score`?  
66. Which numerical features have the **highest negative correlation** with `User_Satisfaction_Rating`?  
67. Create a **scatter plot** of `Price_USD` vs. `Performance_Score` with a **regression line**. Provide the code used.  
68. Create a **scatter plot** of `Battery_Life_Hours` vs. `User_Satisfaction_Rating` with a **regression line**. Provide the code used.  

---

### **(H). GROUPING AND AGGREGATION**  

69. What is the **average** `Price_USD` for each `Category`?  
70. What is the **average** `Battery_Life_Hours` for each `Brand`?  
71. What is the **average** `User_Satisfaction_Rating` for each `Water_Resistance_Rating`?  
72. What is the **maximum** `Performance_Score` for each `App_Ecosystem_Support` category?  
73. What is the **minimum** `Heart_Rate_Accuracy_Percent` for each `Category`?  
74. Group the dataset by `Brand` and calculate the **mean** `Step_Count_Accuracy_Percent`.  
75. Group the dataset by `Category` and calculate the **median** `Sleep_Tracking_Accuracy_Percent`.  
76. Group the dataset by `Connectivity_Features` and calculate the **total count** of devices.  
77. Group the dataset by `App_Ecosystem_Support` and calculate the **average** `Price_USD`.  
78. Group the dataset by `Water_Resistance_Rating` and calculate the **standard deviation** of `Battery_Life_Hours`.  
79. How would you check for **duplicate rows** in the dataset? Provide the code used.  
80. **Remove duplicate rows** from the dataset, if any, and report the number of duplicates removed. Provide the code used.  

---

### **(I). ADVANCED ANALYSIS**  

81. What is the **average** `Performance_Score` for devices with `Water_Resistance_Rating` of **5ATM**?  
82. What is the **average** `User_Satisfaction_Rating` for devices with `Connectivity_Features` including **Bluetooth**?  
83. Which `Brand` has the **highest average** `Heart_Rate_Accuracy_Percent`?  
84. Which `Category` has the **lowest average** `Price_USD`?  
85. Create a **pivot table** showing the average `Performance_Score` by `Brand` and `Category`. Provide the code used.  
86. Create a **pivot table** showing the count of devices by `Water_Resistance_Rating` and `App_Ecosystem_Support`. Provide the code used.  
87. What is the **average** `GPS_Accuracy_Meters` for devices with `Health_Sensors_Count` greater than **8**?  
88. How many devices have a `User_Satisfaction_Rating` above **9.0**?  
89. What is the **distribution** of `Health_Sensors_Count` across all devices? Create a **histogram** to visualize it.  
90. Create a **violin plot** showing the distribution of `Performance_Score` by `Category`. Provide the code used.  
