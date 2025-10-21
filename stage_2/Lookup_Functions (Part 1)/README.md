# Lookup Functions Deep Dive (Part 1)

This lesson introduces Excel lookup functions that help you retrieve data across large tables efficiently. You will learn how to use **VLOOKUP** and **HLOOKUP**, fix common errors, and understand their limitations.

## Topics Covered
- VLOOKUP and HLOOKUP syntax and structure
- Exact and approximate match options
- Common lookup errors and fixes
- Understanding lookup limitations

## Practice File
- [Employee Lookup Tool](./Employee_Lookup_Tool.xlsx) → Dataset for learning and practicing lookup functions

## Key Takeaways
- Use **VLOOKUP** for vertical lookups and **HLOOKUP** for horizontal lookups
- Always ensure your lookup value is in the first column of the range
- Use `FALSE` for exact matches and `TRUE` for approximate matches
- Lookup functions are case-insensitive
- They can break easily if the column order changes

## Limitations
- The lookup value must be in the **first column** of the range
- You **cannot look to the left** of the lookup column
- They **break easily** when columns are moved or inserted
- They are **case-insensitive**
- They can be **slow** for large datasets

## Practice Exercise
Create an employee lookup tool that can:
1. Return the department and salary of an employee by ID
2. Retrieve the performance rating using VLOOKUP
3. Use HLOOKUP for a horizontal data summary


