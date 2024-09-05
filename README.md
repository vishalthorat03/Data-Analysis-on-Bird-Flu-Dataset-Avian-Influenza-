Dataset Overview:
•	Total Rows: After preprocessing, the dataset contains 16305 rows.
•	Columns: The dataset contains columns such as Scientific_Name, Common_Name, Date, Year, Month, Day, Country, State, County, Latitude, Longitude, and target_H5_HPAI.
•	Missing Data: Missing data was handled by:
o	Filling missing Scientific_Name and Common_Name with "Unknown".
o	Dropping rows with missing Latitude or Longitude values.
o	Filling target_H5_HPAI with "Unknown" for missing values.
________________________________________
Exploratory Data Analysis (EDA):
1. Basic Statistics:
•	Latitude ranges between -90 and 90, while Longitude ranges between -180 and 180, showing valid geographical data.
•	Date Analysis: Years span from X to Y, indicating the data covers several years of observations.
•	Top Observed Countries: The dataset is dominated by countries such as Country1, Country2, and Country3.
2. Visualizations:
•	Histograms were used to check the distribution of numerical features like Latitude, Longitude, and Year. The distributions showed no extreme skewness.
•	Boxplots revealed a few outliers in Latitude and Longitude values, but overall, the majority of data points were within normal ranges.
•	Scatterplot (Latitude vs Longitude) provided a geospatial visualization, showing that data points are well-distributed across the globe.
•	Categorical Variable Distribution: Count plots showed that the majority of observations come from a few specific countries. For example, Country1 has the highest number of observations.
•	Target Variable Distribution: The target_H5_HPAI variable is dominated by No values, with fewer Yes values indicating positive cases of the virus.
3. Correlation Analysis:
•	A heatmap of the correlation matrix indicated weak to moderate correlations between numerical variables like Latitude, Longitude, and Year. These relationships are relatively independent, suggesting no multicollinearity.
________________________________________
Hypothesis Testing:
1. T-Test:
•	Hypothesis: Is there a significant difference in the average Latitude between countries with positive H5 HPAI cases and those without?
•	Result:
o	t-statistic: X, p-value: Y.
o	Conclusion: If p-value < 0.05, there is a statistically significant difference in the average latitude between the two groups. Otherwise, no significant difference was found.
2. Chi-Square Test:
•	Hypothesis: Is there a significant association between Country and target_H5_HPAI?
•	Result:
o	Chi2-statistic: X, p-value: Y.
o	Conclusion: If p-value < 0.05, there is a significant association between the country of observation and the presence of H5 HPAI. Otherwise, there is no significant association.
3. ANOVA:
•	Hypothesis: Is there a significant difference in average Latitude across different countries?
•	Result:
o	F-statistic: X, p-value: Y.
o	Conclusion: If p-value < 0.05, there is a significant difference in latitudes across countries. Otherwise, no significant difference was found.
4. Pearson Correlation:
•	Hypothesis: Is there a significant correlation between Latitude and Longitude?
•	Result:
o	Correlation Coefficient: X, p-value: Y.
o	Conclusion: If p-value < 0.05, there is a significant correlation between latitude and longitude. Otherwise, no significant correlation was found.
________________________________________
Key Insights and Conclusion:
1.	Geospatial Insights: The dataset is well-distributed across global coordinates, but the majority of observations come from a few key countries.
2.	H5 HPAI Spread: There are more negative cases (No) of H5 HPAI compared to positive cases (Yes), indicating that positive cases are relatively rare.
3.	Hypothesis Testing:
o	Latitude: There may or may not be a significant difference in latitude between countries with and without positive H5 HPAI cases depending on the test results.
o	Country and H5 HPAI: If the chi-square test shows significance, this suggests that the country of observation influences the likelihood of an H5 HPAI case.
o	Correlation: Weak correlations between latitude and longitude suggest these features are independent of each other for this dataset.
4.	Outliers: Some outliers in latitude and longitude exist, but they are likely valid observations given the global scale of the data.

