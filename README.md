

==============================================================================================================================

## Analyze the Data 

- #### Analysis 1: Missing values -There are many missing values in the data set
- #### Analysis 2: Very high percentage of missing data for many columns which needs to be corrected before Modeling
- #### Analysis 3: Unique Value -After Analyzing unique values for each column, it is found that
		- cylinders has value 'other' which needs to be changed
		- drive has values 4wd as well as fwd which should be changed to one type
		- Many columns has Nan values which needs to be either deleted or imputed 
- #### Analysis 4: Duplicate Records- No duplicate records found in the data set
- #### Analysis 5: Car prices- 36222 cars has price less than $100. This doesn't make sense. Since this number is very less as compared to 4 hundred thousand records,I will delete these records

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
![Low Price](https://github.com/viksaraw/Module-11-Pics/blob/main/Pic%207%20-%20Price%20value%20less%20than%20100.png)

## EDA

### 1. Outlier Analysis
#### Scatter plot for year vs price
![Scatter plot for year vs price](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%20-1.png)
#####  Analysis 1 - Very few outliers on year, so can be ignored 

#### Scatter plot for odometer vs price
![Scatter plot for odometer vs price](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%202%20Scatter%20Plot%20-%20Odometer%20vs%20Price.png)
#### Analysis 2 - Few outliers on year, so can be ignored 

### Histogram plot for year to see cars in each year from the data
![Histogram Query](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%203%20-%20Hist%20for%20year%201.png)
![Histogram pic](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%204%20-%20Hist%20for%20year%202.png)
#### Analysis 3 - Histogram is clearly left skewed. Which means we can ignore the data before 2000

#### Histogram plot for manufacturere
![Histogram query per manufacturer](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%205%20Histogram%20query%20for%20manufacturer.png)
![Histogram per manufacturer](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%206%20Histogram%20for%20manufacturer.png)

#### Box plot for Price to see outliers
![Box plot for price](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%20-%207%20Box%20plot%20Outlier%20analysis.png)

#### Analysis 4: Clearly there are outliers which can be removed, Below I am removing these outliers
![Removing outliers](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA-8%20Outlier%20removed.png)

#### Countplot for fuel
![Countplot for fuel](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA-9%20Countplot%20fuel.png)

#### Countplot for transmission
![Countplot for transmission](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA-10%20Countplot%20transmission.png)







