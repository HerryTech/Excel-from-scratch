# Basic Error Handling & Named Ranges  

This lesson introduces two important beginner concepts: handling common Excel errors and using named ranges for easier formulas. By the end, you will be able to prevent errors from disrupting your analysis and make your formulas cleaner and more understandable.  

## Topics Covered
- Identifying and fixing common errors:  
  - **#DIV/0!** (division by zero)  
  - **#VALUE!** (wrong data type)  
  - **#N/A** (missing lookup values) 
  - **#REF!** (invalid cell reference or deleted cell) 
  - **#NAME?** (unrecognized text or function name)
- Using **IFERROR** and **IFNA** to display custom messages instead of errors  
- Creating **named ranges** for cells or tables to simplify formulas  
- Using named ranges in formulas (e.g., `=SUM(Price)`, `=VLOOKUP(A2, CategoryTable, 2, FALSE)`)  

## Practice Files
- [Basic Error Handling & Named Ranges](./Basic_error_named_ranges.xlsx) → Dataset with products, prices, quantities, revenue, discounts, and lookup table  

## Key Takeaways
- **#DIV/0!** happens when dividing by zero; fix it with `IF(C2=0, "No units", D2/C2)`.  
- **#VALUE!** occurs when using text where numbers are expected; use `ISNUMBER` checks to validate inputs.  
- **#N/A** happens when a lookup value is missing; wrap lookups with `IFNA(..., "Not Found")` to handle it gracefully.  
- Named ranges make formulas easier to read and manage. Instead of `$B$2:$B$21`, you can name it **Price** and simply write `=SUM(Price)`.  
- Lookup tables can be placed alongside the dataset or on a separate sheet. Naming them (e.g., **CategoryTable**) makes formulas cleaner and more reusable.  
