# World Cup Matches Data Cleansing
The dataset comprises information about FIFA World Cup matches, containing details such as the year of the tournament, date and time of the match, stage of the tournament, stadium and city where the match took place, home and away team names, goals scored by each team, attendance, halftime scores, referee details, round ID, match ID, and initials of the home and away teams.

This dataset serves as the basis for analyzing FIFA World Cup matches, allowing for insights into various aspects of the tournament, such as team performances, match outcomes, and attendance trends. Before conducting any analysis, it's essential to perform data cleaning and preprocessing to ensure the dataset's quality and integrity.

## Python Libraries Import
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/53e436d7-163d-440f-afa6-cad4353ff524" /></div>

## Load Data Set
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/fc2a59cd-54b7-4b03-85e5-537de3ccbd98" /></div>

Display the data set that has been loaded
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/05c15cbf-e544-42bf-83e7-5ca6b889df9b" /></div> 

## Data Cleansing
Data cleansing is the process of identifying and correcting errors, inconsistencies, and inaccuracies in a dataset to improve its quality and reliability for analysis. It involves various tasks aimed at ensuring that the data is accurate, complete, and consistent.

### Check Data Condition
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/08a4277b-9fcd-442f-993c-b6f54dcdfd87" /></div>
 
From the description, we can see that some columns have fewer non-null values than the total entries, indicating the presence of null or empty values in the DataFrame. Additionally, we can also observe the data types of each column, where there are columns whose data types are not yet appropriate.

## Check and remove duplicate rows from theData Frame
### keep
- {‘first’, ‘last’, False}, default ‘first’
- Determines which duplicates (if any) to mark.
- first : Mark duplicates as True except for the first occurrence.
- last : Mark duplicates as True except for the last occurrence.
- False : Mark all duplicates as True.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/4b778dbc-a490-43cb-a4cf-073364fe43ad" /></div>
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/70cd9792-21a6-4670-89a7-9d52defc9208" /></div>
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/7cdb3c52-5e4a-451a-8cdd-461da496d6c1" /></div>
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/00d4b5c7-03a1-4525-b51f-667ee430df47" /></div>

Due to the presence of numerous NaN values, our first step will be to drop rows containing NaN values.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/f0e91530-3a6b-4af1-9239-f2844f625332" /></div>

Check Duplicates again
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/b1a6693d-24d5-4db1-95cb-a946855e0869" /></div>

<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/33273a7d-7d4d-4554-9659-f575c75649c7" /></div>
 
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/b8f72212-950c-4a01-953e-96bc205969d4" /></div>
 
Once we have confirmed that the duplicated data is indeed redundant, we can proceed to delete the duplicates.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/a66e5e07-84c1-4567-9afb-6eecb7fdf35d" /></div>

## Convert Dtype
"Convert Dtype" refers to the process of converting the data type of a column in a dataset. This process is often necessary to ensure that the data is in the appropriate format for analysis or visualization.

For example, if a column contains numerical data but is stored as a string, it may be necessary to convert it to a numerical data type (e.g., int or float) to perform mathematical operations or statistical analysis.

Similarly, if a column contains dates or times but is stored as a string or integer, it may be necessary to convert it to a datetime data type to perform date-based analysis or visualization.

In summary, converting data types ensures that the data is in the correct format for analysis and allows for more efficient and accurate data processing.
### Year 
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/91234dc5-117c-4d5e-818a-36070c47cdb3" /></div>

### Datetime
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/bb14c74a-46c9-4080-b32f-21ace0781988" /></div>

### Home Team Goals, Away Team Goals, Attendance, Half-time Home Goals, Half-time Away Goals, RoundID, MatchID
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/661a5adb-4409-49dd-b59e-da737c32b832" /></div>

## Check Percentage Missing Values
"Check Percentage Missing Values" refers to the process of calculating and determining the percentage of missing values in each column of a dataset. This step is essential in data preprocessing and quality assurance, as missing values can impact the accuracy and reliability of analytical results.

To perform this task, the dataset is inspected column by column, and the number of missing values in each column is counted. Then, the percentage of missing values is calculated by dividing the number of missing values by the total number of observations in the dataset and multiplying by 100.

Understanding the percentage of missing values in each column helps data analysts or scientists develop appropriate strategies for handling missing data. Depending on the nature of the missing values and their impact on the analysis, strategies such as imputation (replacing missing values with estimated ones), deletion of rows or columns with missing values, or specialized modeling techniques may be employed to address missing data issues effectively.

In summary, checking the percentage of missing values provides valuable insights into the data quality and guides decision-making regarding data preprocessing and analysis strategies.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/93676067-f011-4dce-9e56-5c04be79722f" /></div>
 
It turns out that only the 'Datetime' column has missing values. Although the number of missing values is not significant, considering that 'Datetime' is a crucial column for analysis, we have decided to retain the missing values in the 'Datetime' column.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/715977fc-1913-4540-98aa-0f17a9b16c85" /></div>

#### Insights and Considerations
- All columns have missing values, with 'Attendance' having the highest number of missing values, totaling 3722.
- Assuming we want to analyze "team performance in matches," some unimportant columns can be dropped.
##### Extremely Important Columns
- Year: The year of the match.
- Home Team Name: The name of the home team.
- Away Team Name: The name of the away team.
- Home Team Goals: The score of the match and the performance of the home team in scoring goals.
- Away Team Goals: The score of the match and the performance of the away team in scoring goals.
- Attendance: The number of spectators in the match.
- Datetime: The date and time of the match. (to be manipulated later)
##### Possibly Important Columns
- Half-time Home Goals: The number of goals scored by the home team in the first half.
- Half-time Away Goals: The number of goals scored by the away team in the first half.
- City: The city where the match took place.
- Stadium: The name of the stadium where the match took place.
- Stage: The stage or phase of the tournament.
- RoundID: The ID of the tournament round.
- MatchID: The ID of the match.
- Win conditions: The conditions for winning the match.
##### Unimportant Columns
- Referee: The name of the match referee.
- Assistant 1: The name of the first assistant referee.
- Assistant 2: The name of the second assistant referee.
- Home Team Initials: The initials of the home team.
- Away Team Initials: The initials of the away team.

## Data Manipulation
Data manipulation involves making changes to the dataset to prepare it for analysis or to extract valuable insights. This process includes tasks such as cleaning the data, transforming its structure, creating new features, and aggregating information.

### Drop Non-Essential Columns
This step involves removing columns from the dataset that are deemed non-essential for the analysis. Non-essential columns are those that do not contribute significantly to the analysis or do not align with the research objectives. By dropping these columns, we can streamline the dataset and focus only on the most relevant features.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/8b3ffc6a-7d9c-4a39-9563-7821bf25eedc" /></div>

We drop columns such as 'Referee', 'Assistant 1', 'Assistant 2', 'Home Team Initials', and 'Away Team Initials' as they are not critical for the analysis at hand.

Show dataset info to see if the date and country columns are missing.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/64eebc71-b9ef-46a1-aafe-59773ed2e525" /></div>

### Make Column Draw, Date, and Time
We will perform data manipulation here. Manipulation here does not involve altering data values but rather restructuring the data to make it easier for machines to read.
To determine whether a match ended in a draw or not, we can use the "Home Team Goals" and "Away Team Goals" columns.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/f6898f05-12c5-4ab2-9aae-861b0c2a1aa7" /></div> 

Split Datetime into 'Date' and 'Time'
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/6d55888c-1254-4b96-9fef-967daa803bef" /></div>

## Visualization
### Home Team Goals vs Away Team Goals 
Analyze the relationship between the number of goals scored by the home team and the number of goals scored by the away team.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/d0cd563d-67b5-4cdb-b9fd-9dcbb89456f0" /></div>
 
Using value_counts() to count how many times each value of home team goals appears in the data, only in matches where the away team scored a goal.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/c9a8ae10-9236-477f-a41c-56fa192d2b9c" /></div>

### Win Conditions vs Home Team Goals
Looking at how victory conditions are based on home team goals
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/90a996e1-b69a-47fe-bf65-e721808aa7b3" /></div>

There are 48 entries in the DataFrame that have 5 or more goals scored by the home team but do not have any information in the 'win conditions' column.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/85ce55ce-52ea-4f5d-bc14-fba216a16012" /></div>

### Number of Matches by Year
- The groupby() function is used to group the rows of data based on the same value in the column used as the grouping criterion, in this case, the 'Year' column.
- The size() method counts the number of rows in each group. In this context, each year group will have the same number of rows as the number of matches in that year.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/62f872d6-4422-4c4c-94ed-5a09d2c99c6f" /></div>

### Year vs Draw
Count of matches that ended in a draw for matches from the year 2000 onwards.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/e466d5b9-323a-4858-90dc-3594c9b22f09" /></div>

## Pivot
Pivoting is a process used to reorganize and reshape data, typically for the purpose of analysis or visualization. In pandas, the `pivot_table()` function is commonly used to create a spreadsheet-style pivot table as a DataFrame. This function allows us to specify the index, columns, and values to aggregate, providing flexibility in how the data is arranged.

By pivoting data, we can transform rows into columns and vice versa, aggregating values based on specified criteria. This can help in summarizing and analyzing data in a more structured and intuitive format, facilitating further exploration and interpretation.

### Make_pivot
The `make_pivot` function is a custom utility developed to pivot the data in our dataset. Pivoting is a technique used to reshape data from long to wide format, making it easier to analyze and visualize. This function takes certain parameters such as index, columns, and aggregation functions to create a pivot table from the original dataset.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/822ce881-443b-4fb1-91b1-8038eb2ee396" /></div>

After observing the bar chart, it seems that visualizing Year vs Draw would be more appropriate using a line graph.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/91376874-dc2f-4dbf-8965-d563151d3131" /></div>

### Slice_pivot
The `slice_pivot` variable is a pivot table generated from a sliced portion of the original dataset. 
This pivot table provides insights into specific aspects of the data by grouping and aggregating values based on specified index and column criteria.
#### Description:
- `Purpose`: To analyze a subset of the dataset and visualize relationships between different variables.
- `Generated From`: The df_slice DataFrame, which is a subset of the original dataset containing selected columns.
- `Parameters`: The pivot table is created using the pivot_table function, with parameters specifying index, columns, and aggregation functions.

#### How many `Draws` based on the `Year`
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/21054a05-64de-48a0-a955-d294a5ff0756" /></div>

#### How many `Draws` occur in each stage of the matches based on the `Year`
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/f79a12de-2018-49e2-b100-3b487e91cfba" /></div>

## Groupby
The `groupby` operation in pandas is a powerful tool for splitting the data into groups based on some criteria, applying a function to each group independently, and then combining the results into a DataFrame or other data structure.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/1e84eb3b-cdfa-4531-bec8-59c62445e0d0" /></div> 

## Crosstab
The `crosstab` function in pandas is used to compute a cross-tabulation of two or more factors, also known as contingency tables. It computes a simple cross-tabulation of two (or more) factors, which can be either categorical or discrete variables.

By default, it calculates the frequency.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/bf265072-a5bc-458b-b7a1-403e28bc48b1" /></div>

## Get Dummies
The `get_dummies` function in pandas is used to convert categorical variables into dummy/indicator variables, also known as one-hot encoding. It creates a new DataFrame with binary indicator variables for each category present in the original categorical variable.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/4711cdf5-e6c9-474c-9235-1483383eed01" /></div>

## Sort
Sorting data in pandas allows you to rearrange the rows of a DataFrame or Series based on the values of one or more columns. The `sort_values` method is commonly used for this purpose.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/cb3d66fa-dce4-42d5-a5f6-bbbb1da43e55" /></div>

## Rename
Renaming columns in pandas allows you to change the names of one or more columns in a DataFrame to make them more descriptive or suitable for analysis. The `rename` method is commonly used for this purpose.
<div align="center"><img src="(https://github.com/alresadeva/Data_Visualization_1/assets/166176480/d5d4328d-c817-43f0-a7d4-6a263ad57400" /></div> 

## Concat
Concatenating DataFrames in pandas involves combining multiple DataFrames along rows or columns. The `concat` function is used for this purpose.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/2e983051-f8b6-40ae-a04d-3ef2d56b6642" /></div>

## Merge
Merging DataFrames in pandas involves combining data from different sources based on common columns or indices. The `merge` function is used for this purpose.
<div align="center"><img src="https://github.com/alresadeva/Data_Visualization_1/assets/166176480/d0219e2d-0178-4c5a-acd1-d6415a372815" /></div>
