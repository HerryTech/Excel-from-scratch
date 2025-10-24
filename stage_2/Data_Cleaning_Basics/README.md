# Data Cleaning Basics  

This lesson is crucial for anyone working with data in Excel. Raw data from various sources (CSV imports, databases, web scraping) is rarely clean and consistent. This module focuses on a suite of powerful text functions designed to remove inconsistencies, standardize formats, and extract specific pieces of information, making your data ready for accurate analysis and reporting.

## Topics Covered

### 1. `TRIM` Function
*   **Purpose:** Removes all leading, trailing, and excessive internal spaces from a text string.
*   **Why it's important:** Extra spaces are often invisible but can cause lookup functions to fail, distort text comparisons, and make your data appear messy. `TRIM` is one of the most frequently used cleaning functions.
*   **Example:** `"  Hello   World  "` becomes `"Hello World"`

### 2. `CLEAN` Function
*   **Purpose:** Removes all non-printable characters from a text string. These are characters that don't display as visible text (e.g., line breaks, carriage returns, control characters) but can be present in data imported from other systems.
*   **Why it's important:** Non-printable characters can interfere with text functions, cause display issues, or prevent data from being correctly interpreted.
*   **Example:** A cell containing "Line1" followed by a hidden line break and "Line2" would be returned as "Line1Line2".

### 3. `PROPER` Function
*   **Purpose:** Converts the first letter of each word in a text string to uppercase and the remaining letters to lowercase.
*   **Why it's important:** Ensures consistent capitalization, which is vital for names, titles, and categories, improving readability and data uniformity.
*   **Example:** `"john doe"` becomes `"John Doe"`, `"the quick brown fox"` becomes `"The Quick Brown Fox"`.

### 4. `LEFT` Function
*   **Purpose:** Extracts a specified number of characters from the *beginning* (left side) of a text string.
*   **Why it's important:** Useful for parsing identifiers, extracting prefixes, or getting the first part of a descriptive text.
*   **Example:** `LEFT("Product Code 123", 7)` returns `"Product"`.

### 5. `RIGHT` Function
*   **Purpose:** Extracts a specified number of characters from the *end* (right side) of a text string.
*   **Why it's important:** Ideal for extracting suffixes, serial numbers, or the last part of a string where the length is known or can be calculated.
*   **Example:** `RIGHT("Order #ABC789", 6)` returns `"ABC789"`.

### 6. `MID` Function
*   **Purpose:** Extracts a specified number of characters from the *middle* of a text string, starting at a given position.
*   **Why it's important:** The most versatile extraction function, allowing you to pull out data segments that are not at the beginning or end, often used in conjunction with `FIND` or `SEARCH`.
*   **Example:** `MID("Invoice-2023-001", 9, 4)` returns `"2023"`.

### 7. `LEN` Function
*   **Purpose:** Returns the total number of characters in a text string, including spaces.
*   **Why it's important:** Crucial for calculating lengths needed by `LEFT`, `RIGHT`, `MID`, and for determining the position of delimiters relative to the end of a string.
*   **Example:** `LEN("  Data  ")` returns `8`.

### 8. `SEARCH` Function
*   **Purpose:** Finds the starting position of one text string within another. It is **not case-sensitive** and supports wildcard characters (`*` for any sequence, `?` for any single character).
*   **Why it's important:** Useful for locating specific characters or substrings when case doesn't matter, or when dealing with variable patterns. Returns an error if not found.
*   **Example:** `SEARCH("code", "Product-Code-XYZ")` returns `9`.

### 9. `FIND` Function
*   **Purpose:** Finds the starting position of one text string within another. It is **case-sensitive** and does **not** support wildcard characters.
*   **Why it's important:** Use when an exact, case-sensitive match for a substring is required, or when `SEARCH`'s wildcard behavior is undesirable. Returns an error if not found.
*   **Example:** `FIND("Code", "Product-Code-XYZ")` returns `9`. `FIND("code", "Product-Code-XYZ")` returns an error (`#VALUE!`).

### 10. `CONCAT` Function (Excel 2016+)
*   **Purpose:** Combines (concatenates) multiple text strings or ranges into a single text string. It is a more modern and flexible alternative to `CONCATENATE`.
*   **Why it's important:** Essential for creating composite keys, summary descriptions, or combined display fields from separate data points.
*   **Example:** `CONCAT("Hello", " ", "World")` returns `"Hello World"`.

### 11. `TEXTJOIN` Function (Excel 2016+)
*   **Purpose:** Combines multiple text strings or ranges, separating them with a specified delimiter and optionally ignoring empty cells.
*   **Why it's important:** Extremely powerful for creating lists from a range of cells, generating comma-separated values (CSV) within a cell, or building complex summary strings with consistent separators.
*   **Example:** If A1="Apple", B1="", C1="Banana", then `TEXTJOIN(", ", TRUE, A1:C1)` returns `"Apple, Banana"`.

## Practice File

-   [Data Cleaning Basics](./Data_cleaning_basics.xlsx) 

## Key Takeaways

* Clean data ensures accurate analysis, reliable lookups, and professional reporting.
* The sequence in which you apply cleaning functions (e.g., `CLEAN` then `TRIM` then `PROPER`) can significantly impact the final result.
* The real power of text cleaning lies in nesting functions (e.g., `TRIM(LEFT(A1, FIND(" ", A1)-1))`) to perform complex transformations.
* Don't be afraid to use intermediate "helper columns" to break down complex cleaning tasks into manageable steps. This improves readability, debugging, and often performance for intricate formulas.
* `SEARCH` is not case-sensitive and allows wildcards, while `FIND` is case-sensitive and exact. Choose the right one for your specific needs.
*   **Beyond Formulas:** For highly repetitive or very complex cleaning on truly massive datasets, consider exploring **Power Query (Get & Transform Data)** in Excel. It's a game-changer for data preparation.