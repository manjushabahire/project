# Cosmetics Product Analysis
## Project Scenario
 Perform data analysis of Cosmetics.CSV, the store wants to understand its product collection better.Provided CSV file to explore the data & share useful findings about product categories, brands, prices, ranking, & skin types.

## Project Objectives
* Understand and clean the dataset whereever it is needed.
* Summarize products, prices, and ratings.
* Create charts to show important patterns.
* Write simple conclusions based on the results.

## Dataset Overview
The file contains 1,472 product records and 11 columns.
These columns include:
- Label (category)
- Brand
- Name
- Price
- Rank
- Ingredients
- Skin-type flags: Combination, Dry, Normal, Oily, and Sensitive. 

# Project Tasks
##  1.Import Required Libraries¶
We will use:

 *Pandas for data manipulation and analysis
*Matplotlib for data visualization


 2. Load the Dataset
The cosmetic product data is stored in a CSV file named cosmetics.csv

We use the read_csv() function from Pandas to load the data into a DataFrame.



# 3. Inspect the Dataset
Before performing analysis, we should understand what the dataset contains.

We will:

*Display the first five rows using head()
*Check column names and data types using info()

# 4. Data Cleaning
Data often contains duplicate records or incorrect data types.

In this dataset:

1. We will remove duplicate rows.
2. We will convert the `Price` column into numeric values.
3. Invalid Price values will be converted into missing values (`NaN`).
4. Missing Price values will be replaced with the median Price.
    
## Convert Price into Numeric Data
The Price column may contain values that are not numeric.

Using pd.to_numeric() with errors="coerce" converts invalid values into NaN.

# Handle Missing Price Values
Missing Price values are replaced using the median Price.

The median is often preferred because it is less affected by extremely high or low Price values.

# 5. Descriptive Statistics
The describe() function provides statistical information about the numerical columns in the dataset.

It includes:

- Count
- Mean
- Standard deviation
- Minimum
- 25th percentile
- Median
- 75th percentile
- Maximum

# 6. Rank-wise Price Analysis
We will calculate the average, minimum, and maximum product price.
The groupby() function groups Label according to their Rank, and mean() calculate the average, max, min,count Price.

## Top 5 Brands in most Label in dataset

## * Highest average rating

# 7. Correlation Analysis

## Correlation between Price & Ranks
Correlation measures the relationship between numerical variables.

The correlation coefficient generally ranges from:

- +1 → Strong positive relationship
- 0 → No linear relationship
- -1 → Strong negative relationship
We use numeric_only=True so that Pandas considers only numerical columns.

## Product Count for each Skin Type

# 8. Data Visualization
Visualization makes it easier to compare Price values across different Ranks.

We will create a bar chart showing the average Price for each Ranks.

# 9. Conclusion  

## * Three important findings

### 1) Category Dominance:
A significant majority of the product belong to a single dominant category.
e.g. Skincare or Makeup, indicating an inventory heavily skewed toward specific consumer needs.

### 2) Price Skewness:
The price distribution is heavily right-skewed, meaning the vast majority of items are budget-friendly, with only a few premium products driving up the maximum range.

### 3) Brand Concentration:
The top 5 brands contribute to a large percentage of the total product count, showing that a few major players command most of the catalog space.

## * Two Practical Recommendations

### 1. Inventory Diversification:
Expand product sourcing in underrepresented categories to capture niche markets & reduce reliance on a single dominant category.

### 2. Tiered Pricing Strategy:
Introduce midtier priced products to bridge the gap between low-cost budget items & highly expensive premium items, capturing mid-range consumer segments.

## * Limitation of the dataset
###  Lack of Performance Metrics:
The dataset lacks transaction history, customer revenue, and profit margin metrics. Consequently, we cannot determine which high-count products or top-ranked brands actually generate the most profit

