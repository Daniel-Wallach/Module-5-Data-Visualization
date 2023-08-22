# Module 5 Challenge - Data Visualization

## Background
You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

## Instructions
This assignment is broken down into the following tasks:
- Prepare the data.
- Generate summary statistics.
- Create bar charts and pie charts.
- Calculate quartiles, find outliers, and create a box plot.
- Create a line plot and a scatter plot.
- Calculate correlation and regression.
- Submit your final analysis.

### Prepare the Data
1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.
2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.
3. Display the updated number of unique mice IDs.

### Generate Summary Statistics
Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.
Your summary statistics should include:
- A row for each drug regimen. These regimen names should be contained in the index column.
- A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

### Create Bar Charts and Pie Charts
1. Generate two bar charts. Both charts should be identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.
   - Create the first bar chart with the Pandas `DataFrame.plot()` method.
   - Create the second bar chart with Matplotlib's `pyplot` methods.
2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.
   - Create the first pie chart with the Pandas `DataFrame.plot()` method.
   - Create the second pie chart with Matplotlib's `pyplot` methods.

### Calculate Quartiles, Find Outliers, and Create a Box Plot
1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:
   - Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.
   - Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.
   - Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.
   - Determine outliers by using the upper and lower bounds, and then print the results.
2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

### Create a Line Plot and a Scatter Plot
1. Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.
2. Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

### Calculate Correlation and Regression
1. Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
2. Plot the linear regression model on top of the previous scatter plot.

---

### Total Number of Timepoints for Each Drug Regimen
#### Pandas
![Number of Observed Timepoints Per Drug Regimen](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/44aa7e7c-dfb0-4dc3-b39e-afbe00ac1164 'Number of Observed Timepoints Per Drug Regimen')

#### Matplotlib
![Number of Observed Timepoints Per Drug Regimen](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/556cfa30-70cb-4862-98f9-fbcd4566c410 'Number of Observed Timepoints Per Drug Regimen')

### Distribution of Mice by Sex
#### Pandas
![Distribution of Female Versus Male Mice](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/5f1513ce-679b-4842-9dbc-111d47c627d6 'Distribution of Mice by Sex')

#### Matplotlib
![Distribution of Female Versus Male Micee](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/066dd6ff-7075-4e38-9f5c-a63dff98f555 'Distribution of Mice by Sex')

### Distrubution of Tumor Volume for Each Treatment Group
![Distrubution of Tumor Volume for Each Treatment Group](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/34289a1f-dd3c-4deb-ac9e-26125d8c4e8a 'Distrubution of Tumor Volume for Each Treatment Group')

### Tumor Volume vs. Time Point for Sample Mouse Treated with Capomulin
![Capomulin treatment of Mouse l509](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/5afe7528-4d0f-4b62-b4ed-a940eafb2481 'Capomulin treatment of Mouse l509')

### Mouse Weight vs. Average Observed Tumor Volume for Entire Capomulin Regimen
![Mouse Weight vs. Average Observed Tumor Volume for Entire Capomulin Regimen](https://github.com/Daniel-Wallach/Module-5-Data-Visualization/assets/44652327/4ec57d81-f299-4dab-ac48-7e273a0aab52 'Mouse Weight vs. Average Observed Tumor Volume for Entire Capomulin Regimen')

---

## References

- [Matplotlub Documentation - Zorder Demo](https://matplotlib.org/stable/gallery/misc/zorder_demo.html)
  
- [Stackoverflow - Python Matplotlib Boxplot Color](https://stackoverflow.com/a/41997956/21718760)


