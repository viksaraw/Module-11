

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

#### Bivariate Analysis
##### Scatter plot between price and odometer
![Price vs Odometer](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA-%2011%20Scatter%20Price%20vs%20odometer.png)

#### Correlation Analysis
##### Correlation plot for numeric data
![Correlation plot for Numeric data](https://github.com/viksaraw/Module-11-Pics/blob/main/EDA%20-12%20Correlation.png)

Analysis:  From the correlation plot, it is clear  that price is positively correlated with year and negatively correlated with odometer.

## Data Preperation
#### After analyzing the data it is clear that this data needs to be prepared before running the models. Below are few steps to prepare the data

1. NaN values
   I found that many columns has NaN or 'NaN' values. The percentage of such records needs to be identified
   <br> Below pic shows the percentage of NaN values for each column
   ![Nan Values](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%201%20-%20Percentage%20of%20NA.png)

2. Many columns like year, model, fuel, odometer, transmission have less than 1.5% of NaN values, so deleting those records won't impact our analysis
   ![Drop NA](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%202%20-%20Dropping%20na%20rows.png)

3. Based upon Business knowledge I know that fea columns like id, VIN, paint_color doesn't impact the price of car. so dropping them
   ![Drop Irrelvant columns](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%203%20-%20Drop%20irrelevant%20columns.png)
   
4. Since we already have model we don't need manufacturer also, so dropping manufacturer
   ![Drop Manufacturer](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%204-%20Drop%20Manufacturer.png)

5. Few columns like size, cylinders, condition, drive, type still have high percentage of NaN values. All the records cannot be deleted. So I will impute them after Train Test Split

Train Test Split
![Train Test Split](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%205-%20Train%20Test%20Split.png)

6. Impute values for columns like size, cylinders, condition, drive, type. Imputation is done based upon the mode from model or group of model and year
   ![Impute Values](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%206%20-%20Imputation%20by%20Model.png)

7. Validate values after Imputation, identify issues if still exists
   ![Validate after Imputation](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%207%20-%20Validate%20values.png)

   Clearly- there are problems in each of these which needs to be fixed individually

8. Fix cylinders - Replace Unknown and other by 6 cylinder, remove word cylinder, convert data type to int
   ![fix cylinder](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%208-%20Fix%20cylinders.png)

9. Fix drive - Replace 4wd with fwd
   ![Fix drive](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%209%20-%20fix%20drive.png)

10. Fix Year - Convert to Age, convert data type to int
    ![Fix year](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%2010%20-%20Year%20to%20Age.png)

11. There are still Non Numeric data which needs to be encoded. My strategy for handling the non numeric data is as follows

     - ['model,'region']:
       After careful consideration-  There are many values for these two columns. It is not advisable
       to go for One Hot or Ordinal Encoding because of performance issues. So after careful consideration I have decided
       that I will **replace them with their average prices**. Meaning I will calculate the average price of each model and 
       replace model with that. Similarly I will calculate the average price of car for each region and replace the region 
       with that.
       
      - ['type', 'transmission', 'drive']
        These columns don't have many values so it is safe to go for **One Hot Encoding** for them

      - ['condition', 'fuel', 'title_status', 'size']
        Thease columns have limited values the values can be sorted in a logical order, so I will be doing **Ordinal 
        Encoding** for them

        **Fixing Model**
        
	![Fix 'model'](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%2011%20-%20Fix%20model.png)

       - Fix Region
         ![Fixing Region](https://github.com/viksaraw/Module-11-Pics/blob/main/Data%20Prep%2014-%20Fix%20region%203.png)
