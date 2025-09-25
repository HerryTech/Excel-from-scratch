# Basic Error Handling & Named Ranges

This lesson combines two important Excel skills: handling common errors in formulas and creating named ranges for easier formulas and cleaner spreadsheets. You will learn how to identify and fix errors like `#DIV/0!`, `#VALUE!`, and `#N/A`, and how to use named ranges instead of cell references.

## Topics Covered
- Identifying common Excel errors:
  - `#DIV/0!` → dividing by zero
  - `#VALUE!` → invalid data type (e.g., text in a number column)
  - `#N/A` → lookup not found
  - Empty cells causing blank or incorrect results  
- Fixing errors with functions:
  - `IFERROR(formula, "message")` → replace errors with text or zero
  - `ISERROR` and `IF` → check for errors and act accordingly
- Creating **Named Ranges**:
  - Naming single cells or multiple ranges
  - Using named ranges in formulas (e.g., `=Price*Quantity` instead of `=B2*C2`)
  - Benefits: clarity, easier formula writing, reusable references

## Key Takeaways
- Excel formulas can break due to missing values, invalid data, or division by zero.
- `IFERROR` is the simplest way to handle common errors and return a clean output.
- Named ranges make formulas more readable and maintainable.
- Combining both skills helps create **error-proof, professional spreadsheets**.
