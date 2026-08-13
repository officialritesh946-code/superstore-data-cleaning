# Superstore Data Cleaning Project

## Project Overview

This project focuses on cleaning and validating the Superstore dataset using Python and Pandas.

The purpose of the project was to identify data-quality issues, remove invalid or duplicate records where necessary, validate numerical and categorical data, investigate potential outliers, and prepare a clean dataset for further analysis.

## Objectives

- Check the dataset structure
- Check for missing values
- Identify and remove duplicate records
- Check text consistency
- Validate data types
- Validate numerical values
- Investigate potential outliers
- Perform final data validation
- Export the cleaned dataset

## Tools Used

- Python
- Pandas
- Google Colab
- Jupyter Notebook
- GitHub

## Dataset

The dataset contains Superstore sales information, including:

- Ship Mode
- Segment
- Country
- City
- State
- Postal Code
- Region
- Category
- Sub-Category
- Sales
- Quantity
- Discount
- Profit

## Data Cleaning Process

### Missing Values

The dataset was checked for missing values.

**Result:** 0 missing values.

No `fillna()` or `dropna()` operation was required.

### Duplicate Records

The dataset originally contained 9,994 rows.

17 exact duplicate rows were identified and removed.

**Final rows: 9,977**

### Text Validation

Text and categorical columns were checked for whitespace and consistency.

No significant formatting issues were identified.

### Data Type Validation

Column data types were checked and found to be appropriate for the data.

No data-type corrections were required.

### Numerical Validation

#### Sales

- Minimum: 0.444
- Maximum: 22,638.48
- Negative Sales values: 0

No invalid negative Sales values were found.

#### Quantity

- Minimum: 1
- Maximum: 14
- Zero Quantity values: 0
- Negative Quantity values: 0

No invalid Quantity values were found.

#### Discount

- Minimum: 0.0
- Maximum: 0.8
- Values below 0: 0
- Values above 1: 0

All Discount values were within the expected range.

#### Profit

- Minimum: -6,599.978
- Maximum: 8,399.976
- Negative Profit records: 1,869
- Zero Profit records: 65

Negative and zero Profit values were retained because they can represent legitimate business outcomes.

## Outlier Analysis

The IQR method was used to identify potential statistical outliers in Sales and Profit.

Potential outliers were investigated rather than automatically removed.

The unusual values appeared to represent legitimate business transactions, such as high-value orders or transactions with high discounts resulting in losses.

Therefore, no statistical outliers were removed without evidence that they were data errors.

## Final Validation

The final dataset was validated after cleaning.

| Check | Result |
|---|---:|
| Original Rows | 9,994 |
| Duplicate Rows Removed | 17 |
| Final Rows | 9,977 |
| Columns | 13 |
| Missing Values | 0 |
| Remaining Duplicates | 0 |

## Final Dataset

The final cleaned dataset contains:

**9,977 rows × 13 columns**

The dataset passed the final validation checks and is ready for further analysis and visualization.

## Project Structure

```text
Superstore-Data-Cleaning/
│
├── data/
│   ├── original_superstore.csv
│   └── cleaned_superstore.csv
│
├── notebooks/
│   └── superstore_data_cleaning.ipynb
│
├── documentation/
│   └── data_cleaning_change_log.md
│
└── README.md