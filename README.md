

==================================================================================================================================================================

## Analyze the Data 

### 1. Load the Data
![Data Load](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%201-%20Data%20Load%20.png)

### 2. Missing data count
##### Analysis 1 : There are many missing values in the data set
![Missing Data](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%202%20-%20Null%20Count.png)

### 3. Missing data percentage
##### Analysis 2 : Percentage of missing data for each column which needs to be corrected before Modeling
![Missing Data Percengate](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%203%20-%20Missing%20Data%20Percentage.png)

### 4. Analyzing unique values for each column
##### Analysis # 3. After Analyzing unique values for each column, it is found that
- cylinders has value 'other' which needs to be changed
- drive has values 4wd as well as fwd which should be changed to one type
- Many columns has Nan values which needs to be either deleted or imputed

![Unique values Analyzed](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%204%20-%20Unique%20value%20analysis.png)
![Unique values Analyzed](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%205%20Unique%20Value%20Analysis.png)

### 5. Analyzing duplicate values
#### Analysis # 4 : No duplicate records found in the data set
![No Duplicates found](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%206%20Duplicate%20Analysis.png)

### 6. Eyeballing Price
#### Analysis # 5 : 36222 cars has price less than $100. This doesn't make sense. Since this number is very less as compared to 4 hundred thousand records,I will delete these records
![Low Price](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%207%20-%20Price%20value%20less.png)
