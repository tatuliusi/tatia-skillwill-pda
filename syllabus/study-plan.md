# Study Plan - Python for Data Analytics

**Total:** 203 contact hours · 38 independent hours · 9 assessment hours = 250 hours  
**Duration:** ~20 weeks

## Schedule

**Session format:**  
- 3h sessions (Mon/Tue): ~1.5h lecture + 1.5h practice  
- 2h sessions (Wed/Thu): ~1h lecture + 1h practice

## Hour Distribution by Module

| # | Module | Credits | Contact | Independent | Assessment | Total | Weeks |
|---|--------|---------|---------|-------------|------------|-------|-------|
| 1 | Python Fundamentals | 2 | 40h | 8h | 2h | 50h | 4 |
| 2 | pandas | 3 | 63h | 10h | 2h | 75h | ~6.5 |
| 3 | numpy | 2 | 40h | 8h | 2h | 50h | 4 |
| 4 | Visualization | 2 | 40h | 8h | 2h | 50h | 4 |
| 5 | Full Data Cycle | 1 | 20h | 4h | 1h | 25h | 2 |
| | **Total** | **10** | **203h** | **38h** | **9h** | **250h** | **~20** |

---

## Module 1 — Python Fundamentals (40h contact · 4 weeks)

**Practice format:** Every session's practice half is a numbered exercise set with increasing difficulty — Easy (🟢), Medium (🟡), Hard (🔴). Students work independently, you circulate and grade in real time. Exercise sets live in `/practicals/module-01/`.

**Homework:** One take-home mini-project per week (due next Monday). Projects live in `/practicals/module-01/homework/`.

---

### Week 1 — Variables, Types, Operators, Strings (Dec 1–4)

**Monday 3h — Setup + Variables + Data Types + Operators**
- Lecture (1.5h):
  - Setup (20 min): Install Python 3, IDE setup (PyCharm/VS Code), first `print()`, running scripts vs REPL — keep it fast, have written setup instructions ready beforehand
  - Variables: naming rules/conventions, assignment, reassignment, `del`
  - Data types: `int`, `float`, `str`, `bool`, `None`. `type()`, dynamic typing
  - Operators: arithmetic (`+ - * / // % **`), comparison (`== != > < >= <=`), logical (`and or not`), precedence rules
- Practice (1.5h): **Exercise Set 01** — 15 problems on variables, types, and operators
  - 🟢 1–5: Assign variables, check types, basic arithmetic
  - 🟡 6–10: Operator precedence puzzles, type-aware calculations (int vs float division)
  - 🔴 11–15: Multi-step computations (currency conversion, distance formulas, compound interest)

**Tuesday 3h — Strings + Type Conversion + Input**
- Lecture (1.5h):
  - String operations: indexing, slicing, concatenation, repetition, `len()`, `in`
  - String methods: `upper()`, `lower()`, `strip()`, `replace()`, `split()`, `join()`, `find()`, `count()`, `startswith()`, `endswith()`
  - f-strings, `.format()`, escape characters
  - Type conversion: `int()`, `float()`, `str()`, `bool()` — what converts to what, common pitfalls
  - `input()` — always returns a string, must convert
- Practice (1.5h): **Exercise Set 02** — 15 problems on strings and conversion
  - 🟢 1–5: Basic slicing, upper/lower, len, concatenation
  - 🟡 6–10: Extract parts of strings, clean messy input, format output
  - 🔴 11–15: Parse structured strings (extract name/age from "Name: John, Age: 25"), validate email format, reverse words

**Wednesday 2h — Conditionals**
- Lecture (1h):
  - `if`, `if-else`, `if-elif-else` — syntax and indentation
  - Nested conditions
  - Complex conditions with `and`, `or`, `not`
  - Ternary expression: `x = a if condition else b`
  - Truthy/falsy values
- Practice (1h): **Exercise Set 03** — 12 problems on conditionals
  - 🟢 1–4: Simple if/else (even/odd, positive/negative, pass/fail)
  - 🟡 5–8: Multi-branch (grade classifier, season from month, BMI category)
  - 🔴 9–12: Nested logic (leap year, triangle validator, tax bracket calculator)

**Thursday 2h — Conditionals Deep Practice + Loop Intro**
- Lecture (1h):
  - Quick review: common conditional mistakes (= vs ==, indentation)
  - `while` loop: syntax, flow, counter pattern
  - `break` and `continue`
  - Infinite loop dangers and safeguards
- Practice (1h): **Exercise Set 04** — 12 problems
  - 🟢 1–4: Simple while loops (countdown, sum 1 to N, multiplication table for one number)
  - 🟡 5–8: break/continue patterns (find first divisible, skip negatives)
  - 🔴 9–12: Accumulator patterns (running average, digit sum, number guessing game)

> **Homework Week 1:** "Personal Data Calculator" — a script that takes user input and performs calculations using variables, types, operators, strings, and conditionals (e.g., BMI calculator with categorization, unit converter, age-to-days calculator). Due Dec 8.

---

### Week 2 — Loops, Lists, Comprehensions (Dec 8–11)

**Monday 3h — For Loops + Loop Patterns**
- Lecture (1.5h):
  - `for` loop: iterating over strings, lists, `range(start, stop, step)`
  - Nested loops
  - `enumerate()` — index + value simultaneously
  - `zip()` — iterate multiple sequences in parallel
  - Loop patterns: accumulator, search, filter, transform
- Practice (1.5h): **Exercise Set 05** — 15 problems on for loops
  - 🟢 1–5: range-based loops (sum, factorial, power), iterate strings
  - 🟡 6–10: enumerate/zip usage, nested loops (multiplication table, pattern printing)
  - 🔴 11–15: FizzBuzz, prime checker, find common elements between two lists

**Tuesday 3h — Lists**
- Lecture (1.5h):
  - Creating lists, indexing, negative indexing, slicing
  - Methods: `append()`, `insert()`, `remove()`, `pop()`, `sort()`, `reverse()`, `extend()`, `index()`, `count()`
  - `in` operator, `len()`, `min()`, `max()`, `sum()`
  - List slicing tricks: copy, reverse, step
  - Modifying lists in loops (and why it's dangerous)
- Practice (1.5h): **Exercise Set 06** — 15 problems on lists
  - 🟢 1–5: Create, append, access, slice
  - 🟡 6–10: Remove duplicates, find second largest, merge sorted lists
  - 🔴 11–15: Rotate list, flatten nested list, implement a simple stack

**Wednesday 2h — List Comprehensions + Tuples**
- Lecture (1h):
  - List comprehensions: `[expr for x in iterable]`
  - Conditional comprehensions: `[expr for x in iterable if condition]`
  - Tuples: creation, immutability, indexing, packing/unpacking
  - Multiple assignment: `a, b = b, a`
  - When to use tuples vs lists
- Practice (1h): **Exercise Set 07** — 12 problems
  - 🟢 1–4: Rewrite loops as comprehensions
  - 🟡 5–8: Conditional comprehensions (filter evens, extract initials)
  - 🔴 9–12: Nested comprehensions, tuple unpacking in loops

**Thursday 2h — Dictionaries + Sets**
- Lecture (1h):
  - Dictionaries: creation, accessing with `[]` and `.get()`, adding, updating, deleting
  - Methods: `keys()`, `values()`, `items()`, `update()`, `pop()`
  - Iterating over dicts
  - Sets: creation, `add()`, `remove()`, union `|`, intersection `&`, difference `-`
  - Dict comprehensions (brief intro)
- Practice (1h): **Exercise Set 08** — 12 problems
  - 🟢 1–4: Create dicts, access values, add/update keys
  - 🟡 5–8: Word frequency counter, invert a dict, merge two dicts
  - 🔴 9–12: Group items by category, find unique elements across lists using sets

> **Homework Week 2:** "Student Grade Analyzer" — read a list of student names and grades (hardcoded as a list of dicts), compute class average, find top/bottom students, categorize by grade letter, count per category, display formatted report. Due Dec 15.

---

### Week 3 — Functions, Errors, Modules (Dec 15–18)

**Monday 3h — Functions**
- Lecture (1.5h):
  - Defining with `def`, calling functions
  - Parameters vs arguments
  - Return values (single, multiple via tuple)
  - Default arguments, keyword arguments
  - `*args`, `**kwargs` (brief intro)
  - Variable scope: local vs global
  - Docstrings (one-line)
- Practice (1.5h): **Exercise Set 09** — 15 problems on functions
  - 🟢 1–5: Write basic functions (is_even, celsius_to_fahrenheit, greet)
  - 🟡 6–10: Functions with defaults/kwargs, return multiple values, recursive factorial
  - 🔴 11–15: Write a mini-library of string utilities, password strength checker, function composition

**Tuesday 3h — Lambda, Map/Filter, Modules**
- Lecture (1.5h):
  - Lambda functions: `lambda x: x * 2`
  - `map()`, `filter()`, `sorted()` with key functions
  - Why these matter (preview: pandas `apply()`, `sort_values(key=)`)
  - Importing modules: `import math`, `from random import randint`, `import datetime`
  - Useful standard library: `math`, `random`, `datetime`, `os`
  - Installing external packages with `pip` (preview for pandas/numpy)
- Practice (1.5h): **Exercise Set 10** — 15 problems
  - 🟢 1–5: Rewrite functions as lambdas, basic map/filter
  - 🟡 6–10: Sort lists of dicts by key, chain map+filter, use math/random modules
  - 🔴 11–15: Custom sort (sort strings by length then alphabetically), process a list of records with map/filter/lambda

**Wednesday 2h — Nested Data Structures + Dict Comprehensions**
- Lecture (1h):
  - Lists of dicts (tabular data — preview of DataFrames)
  - Dicts of lists
  - Accessing deeply nested structures
  - Dict comprehensions: `{k: v for k, v in items}`
  - Real-world data modeling: student records, product catalog, transaction log
- Practice (1h): **Exercise Set 11** — 12 problems
  - 🟢 1–4: Access nested values, add records to a list of dicts
  - 🟡 5–8: Filter/sort a list of dicts, compute stats across records
  - 🔴 9–12: Group records by field, build a report from nested data

**Thursday 2h — Error Handling + Debugging**
- Lecture (1h):
  - Common errors: `SyntaxError`, `TypeError`, `ValueError`, `KeyError`, `IndexError`, `ZeroDivisionError`
  - Reading tracebacks — where to look, what matters
  - `try` / `except` / `else` / `finally`
  - Catching specific exceptions
  - Raising exceptions with `raise`
  - Debugging strategies: print debugging, isolating the problem
- Practice (1h): **Exercise Set 12** — 12 problems
  - 🟢 1–4: Add try/except to existing code, identify error types from messages
  - 🟡 5–8: Write safe versions of functions (safe division, safe type conversion, safe dict access)
  - 🔴 9–12: Debug broken scripts (given 3–4 scripts with bugs, find and fix them)

> **Homework Week 3:** "Contact Book" — a function-based program: add, search, update, delete contacts stored as a list of dicts. Must use functions, error handling, and display formatted output. Due Dec 22.

---

### Week 4 — File I/O, Data Scripts, Review, Assessment (Dec 22–25)

> **Note:** Dec 25 may be affected by holiday. Adjust schedule if needed — shift remaining sessions forward.

**Monday 3h — File I/O (Text, CSV, JSON)**
- Lecture (1.5h):
  - Text files: `open()`, `with` statement, `read()`, `readline()`, `readlines()`, `write()`, `writelines()`
  - File modes: `r`, `w`, `a`, `r+`
  - CSV files: `csv.reader`, `csv.writer`, `csv.DictReader`, `csv.DictWriter`
  - JSON files: `json.load()`, `json.dump()`, `json.loads()`, `json.dumps()`
  - When to use which format
- Practice (1.5h): **Exercise Set 13** — 15 problems on file I/O
  - 🟢 1–5: Read a text file, count lines/words, write output
  - 🟡 6–10: Read CSV with DictReader, filter rows, write filtered CSV
  - 🔴 11–15: Parse JSON data, transform between formats (CSV→JSON, JSON→CSV), merge two CSV files

**Tuesday 3h — Data Processing Scripts**
- Lecture (1.5h):
  - Putting it all together: read → clean → process → analyze → output
  - Code organization: functions for each step, main flow
  - Writing reusable, readable scripts
  - Live coding: build a complete data processing script from scratch
- Practice (1.5h): **Exercise Set 14** — 10 complete mini-scripts
  - 🟢 1–3: Read a file, compute basic stats, write report
  - 🟡 4–7: Filter + aggregate data from CSV, handle missing values, formatted output
  - 🔴 8–10: Multi-file processing (read multiple CSVs, combine, analyze, output summary)

**Wednesday 2h — Module 1 Review**
- Review (1h): Rapid-fire review — one example per topic, focus on connections between concepts
- Practice (1h): **Mixed Exercise Set 15** — 12 problems spanning ALL topics (the best preparation for assessment)
  - Problems require combining multiple concepts: loops + dicts + functions, file I/O + error handling, etc.

**Thursday 2h — Module 1 Assessment**
- **Assessment (2h):** Practical task with observation — write a data processing script demonstrating: variables and types, control flow, data structures, functions with error handling, file I/O (CSV or JSON)

> **Homework Week 4:** "Data Report Generator" — read a CSV dataset, clean the data (handle missing values, fix types), compute statistics (mean, min, max, counts by category), generate a formatted text report saved to a file. Due first day of Module 2.

---

## Module 2 — pandas for Data Analysis (63h contact · Weeks 5–11)

**Practice format:** Exercise sets continue numbering from Module 1 (starting at Set 16). Same 🟢🟡🔴 structure. Exercise sets live in `/practicals/module-02/`.

**Homework:** One take-home project per week. Projects live in `/practicals/module-02/homework/`.

---

### Week 5 — Series, DataFrames, Loading Data (Dec 29 – Jan 1)

> **Note:** New Year week — adjust schedule as needed.

**Monday 3h — Series + DataFrame Fundamentals**
- Lecture (1.5h):
  - What is pandas, why it's the backbone of data analytics in Python
  - `pip install pandas`, `import pandas as pd`
  - Series: creation from lists/dicts, indexing, slicing, vectorized operations, `name` attribute
  - DataFrame: creation from dicts, lists of dicts, nested structures. Structure: rows, columns, index
  - Key attributes: `shape`, `dtypes`, `columns`, `index`, `values`
  - Relationship: DataFrame = collection of Series
- Practice (1.5h): **Exercise Set 16** — 15 problems
  - 🟢 1–5: Create Series/DataFrames, access attributes, basic indexing
  - 🟡 6–10: Series arithmetic, create DataFrame from complex dicts, compare Series operations vs list operations
  - 🔴 11–15: Build a DataFrame from multiple Series, convert between Series and DataFrame, reconstruct a table from raw data

**Tuesday 3h — Loading Data (CSV + Excel) + Exporting**
- Lecture (1.5h):
  - `pd.read_csv()`: `sep`, `header`, `names`, `index_col`, `usecols`, `dtype`, `encoding`, `na_values`, `nrows`, `skiprows`
  - `pd.read_excel()`: `sheet_name`, reading multiple sheets, `engine`
  - Exporting: `to_csv()`, `to_excel()` — `index=False`, `encoding`
  - Quick data check workflow: load → shape → dtypes → head
- Practice (1.5h): **Exercise Set 17** — 15 problems
  - 🟢 1–5: Load CSVs with different separators and encodings, check shape/dtypes
  - 🟡 6–10: Load specific columns, skip rows, set custom headers, load Excel sheet by name
  - 🔴 11–15: Load messy CSVs (mixed separators, bad headers), export filtered results, round-trip CSV→DataFrame→CSV

**Wednesday 2h — Data Exploration**
- Lecture (1h):
  - `head()`, `tail()`, `sample()`, `shape`, `len()`
  - `info()` — dtypes, non-null counts, memory usage
  - `describe()` — numeric and categorical stats, `include='all'`
  - `value_counts()`, `nunique()`, `unique()`
  - Building a data profile checklist
- Practice (1h): **Exercise Set 18** — 12 problems
  - 🟢 1–4: Run exploration methods, interpret output
  - 🟡 5–8: Write a data profile summary from exploration output, identify anomalies
  - 🔴 9–12: Given only `info()` and `describe()` output (no raw data), answer questions about the dataset

**Thursday 2h — Indexing & Selection I (loc, iloc)**
- Lecture (1h):
  - Selecting columns: single (`df['col']`), multiple (`df[['a','b']]`)
  - `loc[]` — label-based: single row, row slice, row+column, callable
  - `iloc[]` — position-based: same patterns with integers
  - Setting values with loc/iloc
  - `at[]`, `iat[]` for single-value access (faster)
- Practice (1h): **Exercise Set 19** — 12 problems
  - 🟢 1–4: Select columns, slice rows with loc/iloc
  - 🟡 5–8: Select row+column combos, compare loc vs iloc on same data
  - 🔴 9–12: Extract specific subsets for analysis (top 10 rows sorted by one column, specific row ranges)

> **Homework Week 5:** "Dataset Explorer" — load a provided CSV, produce a full data profile report (shape, types, nulls, value distributions, describe output), save as a text file. Due Jan 5.

---

### Week 6 — Filtering, Sorting, Column Operations (Jan 5–8)

> **Note:** Jan 7 is Orthodox Christmas — adjust if needed.

**Monday 3h — Boolean Indexing & Filtering**
- Lecture (1.5h):
  - Boolean indexing: single condition (`df[df['age'] > 30]`)
  - Combining conditions: `&` (and), `|` (or), `~` (not) — parentheses required
  - `isin()`, `between()`, `.str.contains()`, `.str.startswith()`
  - `query()` — string-based filtering (cleaner for complex conditions)
  - Negation and edge cases: NaN in boolean filters
- Practice (1.5h): **Exercise Set 20** — 15 problems
  - 🟢 1–5: Single-condition filters, isin with a list
  - 🟡 6–10: Multi-condition filters, between for ranges, str.contains for text search
  - 🔴 11–15: Complex business queries ("find all orders over $100 from customers in region X placed in Q4"), query() vs boolean syntax

**Tuesday 3h — Sorting + Column Operations**
- Lecture (1.5h):
  - `sort_values()`: single column, multi-column, `ascending`, `na_position`
  - `sort_index()`. `nlargest()`, `nsmallest()` — faster than sort+head
  - Adding columns: direct assignment, computed columns, conditional (`np.where`, `np.select`)
  - Renaming: `rename(columns={})`, `columns` assignment
  - Dropping: `drop(columns=[])`, `drop(index=[])`
- Practice (1.5h): **Exercise Set 21** — 15 problems
  - 🟢 1–5: Sort by one/two columns, get top N, add a simple computed column
  - 🟡 6–10: Conditional column creation, rename multiple columns, drop and reorder
  - 🔴 11–15: Create rank columns, percentage-of-total columns, binned categories from numeric data

**Wednesday 2h — apply(), map(), lambda in pandas**
- Lecture (1h):
  - `apply()` on columns (Series) and rows (`axis=1`)
  - `map()` for element-wise Series transformation
  - `replace()` for value mapping
  - Using lambda functions with apply (connecting Module 1 lambdas to pandas)
  - When to use vectorized ops vs apply (performance)
- Practice (1h): **Exercise Set 22** — 12 problems
  - 🟢 1–4: apply simple functions to columns, map values
  - 🟡 5–8: Row-wise apply, lambda with conditionals, replace values using a dict
  - 🔴 9–12: Custom transformations (parse complex strings, categorize with multi-rule logic)

**Thursday 2h — String Operations (.str accessor)**
- Lecture (1h):
  - `.str` accessor: `lower()`, `upper()`, `strip()`, `replace()`, `split()`, `contains()`, `extract()`
  - `len()`, `startswith()`, `endswith()`, `slice()`
  - Chaining string methods
  - Regex basics with `.str.contains()` and `.str.extract()` (intro only)
- Practice (1h): **Exercise Set 23** — 12 problems
  - 🟢 1–4: Clean whitespace, standardize case, check for substrings
  - 🟡 5–8: Split full names into first/last, extract numbers from text, clean phone numbers
  - 🔴 9–12: Parse structured text columns (addresses, product codes), normalize messy categorical values

> **Homework Week 6:** "Sales Analysis Report" — filter sales data by multiple criteria, sort by revenue, create computed columns (profit margin, category rank), clean text columns, export clean dataset. Due Jan 12.

---

### Week 7 — Data Types, Dates, Missing Data (Jan 12–15)

**Monday 3h — Data Type Conversion + Date/Time**
- Lecture (1.5h):
  - `astype()` — converting between types, common pitfalls
  - `pd.to_numeric(errors='coerce')` — safe numeric conversion
  - `pd.to_datetime()` — parsing dates from strings, `format`, `dayfirst`, `errors`
  - `.dt` accessor: `year`, `month`, `day`, `dayofweek`, `hour`, date arithmetic with `Timedelta`
  - Categorical dtype: `astype('category')`, memory savings, ordering
- Practice (1.5h): **Exercise Set 24** — 15 problems
  - 🟢 1–5: Convert string columns to numeric/datetime, extract year/month
  - 🟡 6–10: Handle mixed-type columns with to_numeric(coerce), compute age from birthdate, days between dates
  - 🔴 11–15: Parse multiple date formats in one column, create time-based features (day of week, is_weekend, quarter), set up Categorical with custom order

**Tuesday 3h — Missing Data — Detection + Handling**
- Lecture (1.5h):
  - What is `NaN` / `None`, how they propagate in operations
  - Detection: `isna()`, `notna()`, `isna().sum()`, `isna().mean()` (% missing)
  - Dropping: `dropna()` — `how`, `thresh`, `subset` parameters
  - Filling: `fillna()` — constant, `method='ffill'`/`bfill`, fill with column stats (mean/median/mode)
  - `interpolate()` for numeric sequences
  - Strategy decision tree: when to drop vs fill vs leave
- Practice (1.5h): **Exercise Set 25** — 15 problems
  - 🟢 1–5: Detect nulls, count per column, drop rows with any/all nulls
  - 🟡 6–10: Fill with mean/median per column, forward-fill time series gaps, drop only where key columns are null
  - 🔴 11–15: Group-aware filling (fill with group mean, not global mean), document and justify cleaning decisions for a messy dataset

**Wednesday 2h — GroupBy I — Split-Apply-Combine**
- Lecture (1h):
  - Concept: split by key → apply function → combine results
  - `groupby()` — single column, multiple columns
  - Basic aggregation: `sum()`, `mean()`, `count()`, `min()`, `max()`, `std()`
  - Iterating over groups, `get_group()`
  - Sizing: `size()` vs `count()` (NaN handling difference)
- Practice (1h): **Exercise Set 26** — 12 problems
  - 🟢 1–4: Group by one column, compute sum/mean/count
  - 🟡 5–8: Group by two columns, compare group means, find group with max total
  - 🔴 9–12: Analyze sales by region+product, compute market share per category

**Thursday 2h — GroupBy II — Advanced Aggregation**
- Lecture (1h):
  - `.agg()` — multiple functions per column, different functions per column
  - Named aggregation: `df.groupby('x').agg(total=('col', 'sum'), avg=('col', 'mean'))`
  - `transform()` — returns same-size output (group percentages, z-scores)
  - `filter()` — keep groups that meet a condition
- Practice (1h): **Exercise Set 27** — 12 problems
  - 🟢 1–4: Multiple aggregations on one group, named aggregation
  - 🟡 5–8: transform to add "% of group total" column, filter groups by size
  - 🔴 9–12: Running totals within groups, rank within groups, year-over-year comparison by group

> **Homework Week 7:** "Data Cleaning Challenge" — given a deliberately messy dataset (mixed types, inconsistent dates, missing values, dirty strings), clean it step by step, document every decision, export the clean version. Due Jan 19.

---

### Week 8 — Merging, Combining, Reshaping (Jan 19–22)

> **Note:** Jan 19 is Epiphany — adjust if needed.

**Monday 3h — Merge & Join**
- Lecture (1.5h):
  - `pd.merge()` — `how`: inner (default), left, right, outer
  - `on`, `left_on`, `right_on` for different column names
  - `suffixes` for overlapping column names
  - Merge validation: `validate='one_to_many'` etc.
  - Merge indicator: `indicator=True` to debug joins
  - SQL analogy: merge = JOIN, and when to use which type
- Practice (1.5h): **Exercise Set 28** — 15 problems
  - 🟢 1–5: Inner merge two tables on shared key, left join to keep all rows from one side
  - 🟡 6–10: Merge on different column names, handle duplicates from merge, use indicator to find unmatched rows
  - 🔴 11–15: Multi-table merge (orders + customers + products), self-join, merge with aggregated data

**Tuesday 3h — Concat + Combining Strategies**
- Lecture (1.5h):
  - `pd.concat()` — vertical (`axis=0`) and horizontal (`axis=1`)
  - `ignore_index=True`, handling mismatched columns
  - Combining monthly/quarterly files into one dataset
  - `combine_first()` — patching missing values from another DataFrame
  - When to use merge vs concat vs combine_first
- Practice (1.5h): **Exercise Set 29** — 15 problems
  - 🟢 1–5: Stack DataFrames vertically, concat with ignore_index
  - 🟡 6–10: Concat files with different columns, horizontal concat with aligned index
  - 🔴 11–15: Combine 12 monthly CSVs into one yearly dataset, use combine_first to patch data gaps

**Wednesday 2h — Pivot Tables & Reshaping**
- Lecture (1h):
  - `pivot_table()` — `values`, `index`, `columns`, `aggfunc`, `margins`, `fill_value`
  - `melt()` — wide to long format: `id_vars`, `value_vars`, `var_name`, `value_name`
  - `stack()` / `unstack()` — reshaping multi-level index
  - When data should be wide vs long (analysis vs visualization)
- Practice (1h): **Exercise Set 30** — 12 problems
  - 🟢 1–4: Create basic pivot table, melt a wide table
  - 🟡 5–8: Pivot with multiple aggfuncs, margins=True for totals, reshape survey data
  - 🔴 9–12: Round-trip wide→long→wide, create cross-tabulation, reshape for plotting

**Thursday 2h — Window Functions + Multi-Index**
- Lecture (1h):
  - `rolling()` — moving average, moving sum, window size
  - `expanding()` — cumulative calculations
  - `shift()` — lag/lead for change calculations (day-over-day, pct_change)
  - Multi-index: brief intro — `set_index()` with multiple columns, `reset_index()`, `xs()` for cross-section
- Practice (1h): **Exercise Set 31** — 12 problems
  - 🟢 1–4: 7-day rolling average, cumulative sum, shift to compute daily change
  - 🟡 5–8: pct_change for growth rates, rolling std for volatility, expanding mean vs rolling mean
  - 🔴 9–12: Multi-index groupby results, cross-section selection, build a simple trend analysis

> **Homework Week 8:** "Multi-Source Integration" — merge 3 related datasets (e.g., employees + departments + salaries), handle mismatched keys, create a pivot table summary, compute rolling averages on time-series columns. Due Jan 26.

---

### Week 9 — pandas Practice & Putting It All Together (Jan 26–29)

**Monday 3h — Pandas Plotting + Practice Session I**
- Lecture (1h):
  - `df.plot()` — quick plotting built into pandas (line, bar, hist, scatter, box)
  - `df.plot(kind='bar')`, `df['col'].plot.hist()`, `df.plot.scatter(x, y)`
  - When to use pandas plotting vs matplotlib/seaborn (quick EDA vs polished output)
- Practice (2h): **Exercise Set 32** — 10 end-to-end mini-analyses
  - 🟢 1–3: Load → explore → filter → plot workflow
  - 🟡 4–7: Load → clean → groupby → pivot → plot workflow
  - 🔴 8–10: Load → merge → clean → analyze → export complete pipeline

**Tuesday 3h — Practice Session II — Real Dataset**
- Practice (3h): **Exercise Set 33** — comprehensive dataset analysis
  - Given a real-world dataset (Kaggle-style), perform complete analysis:
  - Load & explore, clean (nulls, types, strings), filter & sort, groupby analysis, merge with supplementary data, create summary pivot, export results
  - Write a 1-page summary of findings

**Wednesday 2h — Module 2 Review**
- Review (1h): Rapid-fire topic review — one key example per topic, focus on connections
- Practice (1h): **Mixed Exercise Set 34** — 12 problems spanning ALL pandas topics
  - Each problem combines 2–3 concepts (merge + groupby, clean + pivot, filter + window)

**Thursday 2h — Module 2 Review (continued) + Assessment Prep**
- Review (0.5h): Address weak spots from Wednesday
- Practice (1.5h): Timed practice — simulate assessment conditions

> **Homework Week 9:** "Comprehensive Pandas Project" — full analysis pipeline on a new dataset, combining every technique learned. This doubles as assessment preparation. Due Feb 2.

---

### Week 10 — pandas Assessment + numpy Begins (Feb 2–5)

**Monday 3h — Module 2 Assessment**
- **Assessment (2h):** Practical task with observation — load a dataset, clean it, perform filtering/sorting/groupby/merge analysis, handle missing data, create a pivot summary, export results
- Buffer (1h): Assessment overflow / debrief

**Tuesday 3h — Introduction to numpy**
- Lecture (1.5h):
  - What is numpy — vectorized computation, C-speed arrays, foundation under pandas
  - Creating arrays: `np.array()`, `np.zeros()`, `np.ones()`, `np.full()`, `np.eye()`
  - Sequences: `np.arange()`, `np.linspace()`
  - Array properties: `shape`, `dtype`, `ndim`, `size`, `itemsize`
  - Array vs list — performance demo with `%timeit`
- Practice (1.5h): **Exercise Set 35** — 15 problems
  - 🟢 1–5: Create arrays of various shapes, check properties, convert lists to arrays
  - 🟡 6–10: Create identity matrices, specific-value arrays, compare array vs list performance
  - 🔴 11–15: Create arrays from mathematical sequences, combine creation methods

**Wednesday 2h — Array Indexing, Slicing, Reshaping**
- Lecture (1h):
  - 1D indexing and slicing (same as lists, but views not copies)
  - 2D indexing: `arr[row, col]`, row/column slicing
  - Fancy indexing with arrays of indices
  - `reshape()`, `ravel()`, `flatten()`, `.T` (transpose)
  - Views vs copies — when changes propagate
- Practice (1h): **Exercise Set 36** — 12 problems
  - 🟢 1–4: Index, slice, reshape basic arrays
  - 🟡 5–8: 2D slicing (extract sub-matrices), transpose, fancy indexing
  - 🔴 9–12: Reshape data for analysis, understand view vs copy behavior

**Thursday 2h — Array Operations + Broadcasting**
- Lecture (1h):
  - Element-wise operations: `+`, `-`, `*`, `/`, `**`, `%`
  - Universal functions (ufuncs): `np.sqrt()`, `np.exp()`, `np.log()`, `np.abs()`, `np.round()`
  - Comparison operations: `>`, `<`, `==` on arrays → boolean arrays
  - Broadcasting rules: scalar+array, 1D+2D, shape compatibility
- Practice (1h): **Exercise Set 37** — 12 problems
  - 🟢 1–4: Element-wise arithmetic, apply ufuncs
  - 🟡 5–8: Normalize data (subtract mean, divide by std), broadcast 1D across 2D
  - 🔴 9–12: Vectorized distance calculations, temperature conversion on a matrix, broadcasting edge cases

> **Homework Week 10:** "numpy Warm-up" — create arrays from formulas, perform vectorized computations that would be slow with loops, compare execution times. Due Feb 9.

---

## Module 3 — numpy for Numerical Computing (40h contact · Weeks 10 Tue – 14)

**Practice format:** Exercise sets continue (starting at Set 35). Sets live in `/practicals/module-03/`.

**Note:** Module 3 starts mid-week (Tuesday of Week 10) since pandas assessment takes Monday. Week numbering continues sequentially.

---

### Week 11 — Statistics & Boolean Operations (Feb 9–12)

**Monday 3h — Statistical Functions I**
- Lecture (1.5h):
  - `np.mean()`, `np.median()`, `np.std()`, `np.var()`
  - The `axis` parameter: `axis=0` (along rows = per column), `axis=1` (along columns = per row)
  - `np.min()`, `np.max()`, `np.argmin()`, `np.argmax()` — values and positions
  - `np.sum()`, `np.cumsum()`, `np.cumprod()`
  - `np.percentile()`, `np.quantile()` — distribution analysis
- Practice (1.5h): **Exercise Set 38** — 15 problems
  - 🟢 1–5: Compute mean/std/min/max on 1D arrays, interpret results
  - 🟡 6–10: Use axis parameter on 2D data (per-student vs per-subject stats), find positions of extremes
  - 🔴 11–15: Build a full descriptive statistics function, compute percentile ranks, compare distributions

**Tuesday 3h — Statistical Functions II + Correlation**
- Lecture (1.5h):
  - `np.corrcoef()` — correlation matrix
  - `np.cov()` — covariance matrix
  - Interpreting correlation: strong/weak, positive/negative
  - `np.histogram()` — binning data programmatically
  - `np.digitize()` — assign data to bins
  - Weighted statistics: `np.average(weights=)`
- Practice (1.5h): **Exercise Set 39** — 15 problems
  - 🟢 1–5: Compute correlation between two arrays, interpret sign and strength
  - 🟡 6–10: Build correlation matrix for multiple variables, bin continuous data, weighted average
  - 🔴 11–15: Identify most/least correlated pairs in a matrix, compute running correlation, statistical comparison of groups

**Wednesday 2h — Boolean Operations & Masking**
- Lecture (1h):
  - Boolean arrays from comparisons (`arr > 5` → `[True, False, ...]`)
  - Boolean indexing: `arr[arr > 0]` — filtering arrays
  - `np.where(condition, x, y)` — vectorized if-else
  - `np.any()`, `np.all()` — testing conditions across arrays
  - Combining conditions: `&`, `|`, `~` on boolean arrays
  - `np.count_nonzero()` — counting True values
- Practice (1h): **Exercise Set 40** — 12 problems
  - 🟢 1–4: Create boolean masks, filter arrays, count matches
  - 🟡 5–8: np.where for conditional replacement, combine multiple conditions
  - 🔴 9–12: Outlier detection (values beyond 2 std), flag and replace anomalies, multi-condition data cleaning

**Thursday 2h — Random Numbers & Simulation**
- Lecture (1h):
  - `np.random.default_rng()` — modern random generator
  - Uniform: `rng.random()`, `rng.integers()`. Normal: `rng.normal()`
  - Other distributions: `rng.choice()`, `rng.shuffle()`, `rng.permutation()`
  - Seeds for reproducibility: `np.random.default_rng(seed=42)`
  - Sampling: `rng.choice(arr, size, replace=False)`
- Practice (1h): **Exercise Set 41** — 12 problems
  - 🟢 1–4: Generate random arrays (uniform, normal), set seed for reproducibility
  - 🟡 5–8: Simulate coin flips/dice rolls, random sampling from a dataset, bootstrap sampling
  - 🔴 9–12: Monte Carlo estimation of pi, simulate random walks, A/B test simulation

> **Homework Week 11:** "Statistical Analysis Report" — given a dataset as arrays, compute all descriptive stats, correlation matrix, identify outliers, run a simple simulation, write up findings. Due Feb 16.

---

### Week 12 — Linear Algebra, Integration, Practice (Feb 16–19)

**Monday 3h — Linear Algebra Basics + Sorting/Searching**
- Lecture (1.5h):
  - Dot product: `np.dot(a, b)`, `a @ b`
  - Matrix multiplication: `np.matmul()`, `@` operator
  - `np.linalg.inv()` (inverse), `np.linalg.det()` (determinant) — conceptual, not deep math
  - Solving linear systems: `np.linalg.solve(A, b)`
  - Sorting: `np.sort()`, `np.argsort()` — sort and get sorted indices
  - Searching: `np.searchsorted()`, `np.unique()`
- Practice (1.5h): **Exercise Set 42** — 15 problems
  - 🟢 1–5: Dot product, matrix multiply, sort arrays
  - 🟡 6–10: Solve 2×2 and 3×3 systems, argsort for ranking, unique values with counts
  - 🔴 11–15: Portfolio return calculation (weights @ returns), sort rows of a 2D array by one column

**Tuesday 3h — numpy + pandas Integration**
- Lecture (1.5h):
  - numpy arrays as the backbone of DataFrames (`.values`, `.to_numpy()`)
  - Vectorized operations on DataFrame columns using numpy functions
  - `np.where()` and `np.select()` for conditional columns in pandas
  - Performance: numpy vectorization vs pandas apply vs Python loops (benchmark)
  - Converting between numpy arrays and DataFrames
- Practice (1.5h): **Exercise Set 43** — 15 problems
  - 🟢 1–5: Use np.where in pandas, extract numpy array from DataFrame
  - 🟡 6–10: Vectorized column creation, np.select for multi-condition columns, performance comparison
  - 🔴 11–15: Optimize a slow pandas pipeline with numpy, batch statistical computations on DataFrames

**Wednesday 2h — Practice Session — End-to-End Analysis**
- Practice (2h): **Exercise Set 44** — 8 comprehensive problems
  - Each problem: given a scenario and data, use numpy to compute, interpret, and explain results
  - Focus on interpretation: "what does this correlation mean?", "is this outlier real?"

**Thursday 2h — Practice Session II**
- Practice (2h): **Exercise Set 45** — mixed numpy + pandas problems
  - Problems require choosing the right tool (numpy vs pandas) for each sub-task
  - Build a mini statistical report combining both libraries

> **Homework Week 12:** "numpy Performance Challenge" — rewrite 5 slow Python/pandas operations using numpy vectorization, benchmark each, explain the speedup. Due Feb 23.

---

### Week 13 — numpy Review & Assessment (Feb 23–26)

**Monday 3h — Advanced Topics + Practice**
- Lecture (1h):
  - `np.vectorize()` — wrapping custom functions for arrays
  - Structured arrays (brief intro — arrays with named fields)
  - `np.set_printoptions()` — controlling output display
  - Best practices: avoid loops, use broadcasting, choose the right dtype
- Practice (2h): **Exercise Set 46** — 12 problems spanning all numpy topics
  - Problems require combining: array creation + operations + statistics + boolean masking + interpretation

**Tuesday 3h — Module 3 Review**
- Review (1.5h): Rapid-fire review of all numpy topics, one key example each
- Practice (1.5h): **Mixed Exercise Set 47** — 12 problems, timed
  - Every problem combines 2–3 numpy concepts
  - Focus on the assessment format: compute + interpret + explain

**Wednesday 2h — Module 3 Assessment Prep**
- Review (0.5h): Address remaining weak spots
- Practice (1.5h): Assessment simulation — work through a complete numpy analysis under time pressure

**Thursday 2h — Module 3 Assessment**
- **Assessment (2h):** Practical task with observation — create arrays, perform mathematical and statistical operations, interpret and explain results in context

> **Homework Week 13:** None — focus on assessment prep.

---

## Module 4 — Data Visualization (40h contact · Weeks 14–17)

**Practice format:** Exercise sets continue (starting at Set 48). Sets live in `/practicals/module-04/`.

**Note:** Every exercise in this module produces a saved chart (`.png`). Students build a portfolio of visualizations.

---

### Week 14 — matplotlib Fundamentals (Mar 2–5)

> **Note:** Mar 3 is Mother's Day — adjust if needed.

**Monday 3h — matplotlib Basics + Line Charts**
- Lecture (1.5h):
  - `import matplotlib.pyplot as plt`, the pyplot interface
  - Figure and Axes objects: `fig, ax = plt.subplots()`
  - Basic line plot: `ax.plot(x, y)`, `plt.show()`, `fig.savefig()`
  - Customization: color, linewidth, linestyle, marker, label
  - Multiple lines on one plot, `ax.legend()`
  - Labels: `ax.set_xlabel()`, `ax.set_ylabel()`, `ax.set_title()`
- Practice (1.5h): **Exercise Set 48** — 15 problems
  - 🟢 1–5: Basic line plot, add title/labels, change colors, save figure
  - 🟡 6–10: Multiple lines with legend, customize markers/styles, plot mathematical functions
  - 🔴 11–15: Multi-line time series comparison (temperature across cities), annotated line chart with key events marked

**Tuesday 3h — Bar Charts + Scatter Plots**
- Lecture (1.5h):
  - Vertical bars: `ax.bar()`. Horizontal: `ax.barh()`
  - Grouped bars (side-by-side with offset), stacked bars (`bottom` parameter)
  - Adding value labels on bars
  - Scatter plots: `ax.scatter(x, y)`, `c` for color, `s` for size, `alpha` for transparency
  - Color mapping for 3rd dimension, colorbar
  - Identifying correlation visually from scatter
- Practice (1.5h): **Exercise Set 49** — 15 problems
  - 🟢 1–5: Simple bar chart, horizontal bars, basic scatter
  - 🟡 6–10: Grouped bars comparing categories, scatter with color-coded groups, bar with value labels
  - 🔴 11–15: Stacked bar showing composition, bubble chart (scatter with size), scatter with trend line

**Wednesday 2h — Histograms + Box Plots**
- Lecture (1h):
  - Histograms: `ax.hist()`, `bins`, `density`, `alpha` for overlapping
  - Understanding distribution shapes: normal, skewed, bimodal
  - Box plots: `ax.boxplot()` — quartiles, whiskers, outliers
  - Violin plots: `ax.violinplot()` — distribution shape + box plot combined
  - When to use each: continuous distribution analysis
- Practice (1h): **Exercise Set 50** — 12 problems
  - 🟢 1–4: Basic histogram with different bin counts, single box plot
  - 🟡 5–8: Overlapping histograms comparing two groups, side-by-side box plots
  - 🔴 9–12: Identify distribution type from histogram, compare groups using box plots, combined histogram + box plot layout

**Thursday 2h — Pie Charts, Heatmaps, Other Types**
- Lecture (1h):
  - Pie charts: `ax.pie()`, `autopct`, `explode` — and when NOT to use them (almost always)
  - Heatmaps: `ax.imshow()` or `ax.pcolormesh()` with `colorbar`
  - Area plots, step plots, error bars (`ax.errorbar()`)
  - Choosing chart type: a decision framework based on what you want to show
- Practice (1h): **Exercise Set 51** — 12 problems
  - 🟢 1–4: Pie chart with percentages, basic heatmap from a matrix
  - 🟡 5–8: Heatmap of correlation matrix with labels, area chart for cumulative data
  - 🔴 9–12: Given a dataset, choose the RIGHT chart type (not pie!), justify your choice, create it

> **Homework Week 14:** "Chart Portfolio Part 1" — create one polished example of each chart type learned this week (line, bar, scatter, histogram, box plot, heatmap), saved as separate PNGs with descriptive filenames. Due Mar 9.

---

### Week 15 — Customization, Subplots, seaborn (Mar 9–12)

> **Note:** Mar 8 is Women's Day (observed) — adjust if needed.

**Monday 3h — Plot Customization Deep Dive**
- Lecture (1.5h):
  - Figure size: `fig, ax = plt.subplots(figsize=(10, 6))`
  - Colors: named, hex, RGB tuples, colormaps (`plt.cm`)
  - Fonts: `fontsize`, `fontweight`, `fontfamily`
  - Grid: `ax.grid()`, `ax.set_axisbelow(True)`, grid styling
  - Ticks: `ax.set_xticks()`, `ax.set_xticklabels()`, rotation, formatting
  - Annotations: `ax.annotate()`, `ax.text()`, arrows
  - Spines: `ax.spines['top'].set_visible(False)` — clean minimal look
  - Matplotlib styles: `plt.style.use('seaborn-v0_8')`, custom rcParams
- Practice (1.5h): **Exercise Set 52** — 15 problems
  - 🟢 1–5: Set figure size, change colors, add grid, rotate tick labels
  - 🟡 6–10: Annotate specific data points, remove top/right spines, apply a style
  - 🔴 11–15: Take a raw chart and make it publication-ready (full makeover: colors, fonts, annotations, clean layout)

**Tuesday 3h — Subplots + Layouts**
- Lecture (1.5h):
  - `plt.subplots(nrows, ncols)` — grid of axes
  - `fig.suptitle()` for overall title
  - Sharing axes: `sharex=True`, `sharey=True`
  - `plt.tight_layout()`, `fig.subplots_adjust()`
  - `GridSpec` for custom layouts (unequal subplot sizes)
  - Inset axes: `ax.inset_axes()` for zoom or mini-charts
- Practice (1.5h): **Exercise Set 53** — 15 problems
  - 🟢 1–5: 2×2 grid of different chart types, shared axes
  - 🟡 6–10: Dashboard-style layout (big chart + small charts), tight_layout
  - 🔴 11–15: Custom GridSpec layout, build a 4-panel analysis dashboard for a dataset

**Wednesday 2h — Introduction to seaborn**
- Lecture (1h):
  - What is seaborn — statistical visualization built on matplotlib
  - Built-in themes: `sns.set_theme()`, palettes
  - Distribution plots: `sns.histplot()`, `sns.kdeplot()`, `sns.ecdfplot()`
  - Relational: `sns.scatterplot()`, `sns.lineplot()` — with `hue`, `size`, `style`
  - Categorical: `sns.barplot()`, `sns.boxplot()`, `sns.violinplot()`, `sns.stripplot()`
- Practice (1h): **Exercise Set 54** — 12 problems
  - 🟢 1–4: Recreate matplotlib charts with seaborn (less code, better defaults)
  - 🟡 5–8: Use hue/size for multi-variable encoding, KDE overlay on histogram
  - 🔴 9–12: Combined plots (violin + strip, hist + kde), compare matplotlib vs seaborn approaches

**Thursday 2h — seaborn Advanced**
- Lecture (1h):
  - Figure-level functions: `sns.catplot()`, `sns.relplot()`, `sns.displot()` — faceting with `col`, `row`
  - `sns.pairplot()` — multi-variable exploration
  - `sns.heatmap()` — annotated correlation matrices, custom colormaps
  - `sns.jointplot()` — scatter + marginal distributions
  - `sns.clustermap()` — hierarchical clustering heatmap (brief)
- Practice (1h): **Exercise Set 55** — 12 problems
  - 🟢 1–4: Pairplot, faceted catplot
  - 🟡 5–8: Annotated heatmap, jointplot, faceted displot
  - 🔴 9–12: Multi-panel EDA dashboard using seaborn, full dataset exploration with pairplot + heatmap + catplot

> **Homework Week 15:** "Chart Portfolio Part 2" — recreate all Part 1 charts using seaborn where applicable, plus create a pairplot, faceted plot, and annotated heatmap. Due Mar 16.

---

### Week 16 — Chart Selection, Interpretation, Practice (Mar 16–19)

**Monday 3h — Choosing the Right Chart + Pandas Plotting**
- Lecture (1.5h):
  - Decision framework: what are you showing?
    - Comparison → bar, grouped bar
    - Distribution → histogram, box plot, violin
    - Relationship → scatter, line (time-based)
    - Composition → stacked bar, (not pie)
    - Trend → line, area
  - Common mistakes: 3D charts, dual y-axes pitfalls, misleading scales, truncated axes
  - Pandas `.plot()` shortcut: `df.plot(kind='bar')`, `df['col'].plot.hist()` — quick EDA tool
  - Color accessibility: colorblind-safe palettes
- Practice (1.5h): **Exercise Set 56** — 15 problems
  - 🟢 1–5: Given data, choose the correct chart type and create it
  - 🟡 6–10: Spot what's wrong with given (bad) charts, fix them
  - 🔴 11–15: Given a dataset with 5+ columns, choose 3 charts that together tell a complete story, create them, write a one-paragraph insight for each

**Tuesday 3h — Visual Interpretation & Communication**
- Lecture (1.5h):
  - Reading charts critically: what story does the data tell?
  - Identifying: trends, outliers, clusters, anomalies, seasonality
  - Writing data insights: observation → evidence → implication
  - Structuring a visual analysis: headline finding → supporting charts → details
  - Presentation tips: one message per chart, label clearly, don't over-decorate
- Practice (1.5h): **Exercise Set 57** — 10 interpretation problems
  - 🟢 1–3: Given charts, write 2-sentence insights
  - 🟡 4–7: Given data + charts, identify what's misleading or could be shown better
  - 🔴 8–10: Given a dataset and a question ("Is sales growing?"), create the chart, interpret it, write a business recommendation

**Wednesday 2h — Practice Session — End-to-End Visual Analysis**
- Practice (2h): **Exercise Set 58** — comprehensive visualization project
  - Given a real dataset: explore with pandas, create 5+ charts using matplotlib and seaborn, write a visual analysis report
  - Must include: distribution plot, comparison plot, relationship plot, trend plot, and a multi-panel dashboard

**Thursday 2h — Module 4 Review**
- Review (1h): Rapid-fire review of all visualization topics
- Practice (1h): **Mixed Exercise Set 59** — 12 problems spanning all chart types and both libraries

---

### Week 17 — Visualization Review & Assessment + Capstone Begins (Mar 23–26)

**Monday 3h — Module 4 Review (continued) + Assessment Prep**
- Review (1h): Address weak areas from Thursday review
- Practice (2h): Assessment simulation — timed, full visual analysis workflow

**Tuesday 3h — Module 4 Assessment**
- **Assessment (2h):** Practical task with observation — given a dataset, create appropriate visualizations with matplotlib/seaborn, customize them for clarity, choose correct chart types, and write interpretation of results
- Buffer (1h): Assessment overflow / debrief

**Wednesday 2h — Capstone Introduction**
- Lecture (1h):
  - Full data processing pipeline overview: load → clean → analyze → visualize → present
  - What makes a good capstone: clear question, clean methodology, insightful visualization, structured presentation
  - Dataset options and selection criteria
- Workshop (1h): Browse datasets, choose one, define analysis questions

**Thursday 2h — Capstone: Dataset Selection + Project Plan**
- Workshop (2h):
  - Finalize dataset choice
  - Write project outline: questions to answer, expected analysis steps, planned visualizations
  - Initial data loading and first exploration
  - **Deliverable:** Project plan document

> **Homework Week 17:** "Dataset Deep Dive" — load your capstone dataset, run full exploration (info, describe, value_counts for every column), identify all data quality issues, write a 1-page data quality assessment. Due Mar 30.

---

## Module 5 — Full Data Processing Cycle (20h contact · Weeks 18–19)

**Format:** No exercise sets — this module is entirely project-based. Students work on their capstone project with instructor guidance. All work is in `/practicals/module-05/capstone/`.

---

### Week 18 — Capstone: Building the Pipeline (Mar 30 – Apr 2)

**Monday 3h — Data Loading & Cleaning**
- Workshop (3h):
  - Load dataset, handle encoding/format issues
  - Clean: missing data strategy (document every decision), fix dtypes, standardize text columns, handle duplicates
  - Create a "clean" version of the dataset
  - Instructor circulates, reviews cleaning decisions

**Tuesday 3h — Data Analysis**
- Workshop (3h):
  - Filtering and subsetting for focused analysis
  - GroupBy analysis: segment data by meaningful categories
  - Statistical computations with numpy: means, correlations, distributions
  - Merge supplementary data if applicable
  - Document key findings as they emerge

**Wednesday 2h — Data Visualization**
- Workshop (2h):
  - Create visualizations for each key finding
  - Choose appropriate chart types (apply Module 4 framework)
  - Customize for clarity: titles, labels, annotations
  - Build a cohesive visual narrative

**Thursday 2h — Visualization + Results Structuring**
- Workshop (2h):
  - Continue/polish visualizations
  - Structure analysis results: executive summary → methodology → findings → conclusions
  - Start building presentation materials

> **Homework Week 18:** Finish any incomplete analysis and polish all visualizations. Due Apr 6.

---

### Week 19 — Capstone: Presentation & Final Assessment (Apr 6–9)

**Monday 3h — Presentation Prep + Peer Review**
- Workshop (1.5h):
  - Finalize presentation: structure the data story (problem → approach → findings → so what?)
  - Practice presenting — focus on explaining code logic and interpreting results
- Peer review (1.5h):
  - Exchange projects with a partner
  - Review checklist: Is the data clean? Are chart types appropriate? Are findings justified? Is the code readable?
  - Give written feedback

**Tuesday 3h — Presentations**
- Presentations (3h):
  - Each student presents their complete data analysis pipeline (5–8 min each)
  - Must demonstrate: data loading, cleaning decisions, pandas+numpy analysis, visualization, interpretation
  - Class Q&A after each presentation

**Wednesday 2h — Final Assessment**
- **Final Assessment (1h):** Individual practical task — given a small new dataset, perform a complete mini-analysis (load → clean → analyze → visualize → interpret) demonstrating integration of all libraries
- Wrap-up (1h): Course recap, what to learn next (SQL, machine learning, dashboarding), resources for continued practice, certificates

**Thursday 2h — Buffer / Overflow**
- Buffer for: presentation overflow, assessment makeup, individual feedback sessions, or additional Q&A
- If not needed: advanced topics preview (SQL with Python, intro to scikit-learn, Plotly for interactive charts)

---

## Notes

- Holiday weeks may require schedule adjustments (Christmas, New Year, Epiphany, Mother's Day, Women's Day)
- Each session's practice half uses numbered exercise sets (🟢🟡🔴) for structured grading — sets live in `/practicals/module-XX/`
- Homework is one take-home project per week — projects live in `/practicals/module-XX/homework/`
- Independent study hours (38h total) cover homework, documentation reading, and extra practice
- Datasets should progress from clean/simple (Module 2) to messy/complex (Module 4–5)
- Exercise sets total: 59 structured sets + capstone project across all modules
