# Data Cleaning Change Log

## Dataset
Superstore Dataset

## Original Dataset
- Rows: 9,994
- Columns: 13

## Cleaning Performed

### 1. Missing Values
- Missing values found: 0
- Action: No action required.
- Reason: The dataset contained no missing values.

### 2. Duplicate Records
- Duplicate rows found: 17
- Duplicate rows removed: 17
- Final rows: 9,977

### 3. Text Validation
- Checked text columns for whitespace and consistency.
- No significant formatting issues were found.
- No changes were required.

### 4. Data Type Validation
- Data types were checked for all columns.
- Numerical columns had appropriate numerical data types.
- No data-type corrections were required.

### 5. Quantity Validation
- Minimum Quantity: 1
- Maximum Quantity: 14
- Zero Quantity: 0
- Negative Quantity: 0
- Result: Valid.

### 6. Discount Validation
- Minimum Discount: 0.0
- Maximum Discount: 0.8
- Values below 0: 0
- Values above 1: 0
- Result: Valid.

### 7. Sales Validation
- Minimum Sales: 0.444
- Maximum Sales: 22,638.48
- Negative Sales: 0
- Result: No invalid Sales values were found.

### 8. Profit Validation
- Minimum Profit: -6,599.978
- Maximum Profit: 8,399.976
- Negative Profit records: 1,869
- Zero Profit records: 65
- Result: Negative and zero Profit values were retained because they can represent legitimate business outcomes.

### 9. Outlier Analysis
- IQR method was used to identify potential outliers.
- Potential outliers were investigated.
- No evidence showed that these values were data-entry errors.
- Legitimate business outliers were retained.

## Final Validation

- Final rows: 9,977
- Final columns: 13
- Missing values: 0
- Duplicate rows: 0

## Final Result

The dataset was successfully cleaned and validated.

The only direct modification made to the dataset was the removal of 17 exact duplicate records.
