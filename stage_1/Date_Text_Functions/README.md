# Date and Text Functions

This section introduces Excel’s date and text functions, which allow you to manipulate time-based data and clean or restructure text entries. These functions are essential for preparing datasets, standardizing information, and extracting insights during analysis.

## Topics Covered
- Using `TODAY()` and `NOW()` to display the current date and time
- Extracting components of a date with `DAY()`, `MONTH()`, and `YEAR()`
- Calculating durations with `DATEDIF` (e.g., age, tenure)  
  - `=DATEDIF(start_date, end_date, "Y")` → difference in years  
  - `=DATEDIF(start_date, end_date, "M")` → difference in months  
  - `=DATEDIF(start_date, end_date, "D")` → difference in days  
  - `=DATEDIF(start_date, end_date, "YM")` → remaining months after last full year  
  - `=DATEDIF(start_date, end_date, "MD")` → remaining days after last full month  
  - `=DATEDIF(start_date, end_date, "YD")` → difference in days ignoring years  
- Joining text with `CONCAT` or `&`
- Changing text case with `UPPER()`, `LOWER()`, and `PROPER()`
- Removing extra spaces with `TRIM()`
- Extracting parts of text with `LEFT()`, `RIGHT()`, and `MID()`
- Finding positions of characters in text with `FIND()` and `SEARCH()`
- Counting characters with `LEN()`

## Practice Files
- [Date_Text_Functions](./Date_Text_Functions.xlsx) — dataset with employee records, dates of joining, product names, and IDs for practicing date and text functions
- [Date_Text_Functions](./Date_Text_Functions.csv) — raw dataset export for external tools

## Key Takeaways
- Date functions make it easy to calculate durations and extract specific components of a date
- `DATEDIF` allows calculation of differences in years, months, or days between two dates
- Text functions help clean and standardize messy datasets for analysis
- Combining text functions allows restructuring of names, IDs, and codes
- Functions like `TRIM`, `PROPER`, and `LEN` improve data quality and consistency
- These tools are vital for cleaning and preparing raw data before analysis

