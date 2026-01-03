# D598 Task 2 — Equity Fund Data Analysis (Python / pandas)

This project analyzes a quarterly dataset of 150 U.S. businesses for an equity fund rebalancing exercise.  
It performs data loading, validation checks, state-level descriptive statistics, leverage screening, and feature engineering (debt-to-income ratio).

---

## Project Objectives (Task Requirements)

This program completes the following tasks:

1. **Import the data file into a DataFrame**
2. **Identify duplicate rows** in the dataset
3. **Group businesses by state** and compute **descriptive statistics** (mean, median, min, max) for **all numeric variables** by state, stored as a new DataFrame
4. **Filter businesses with negative Debt-to-Equity ratios**
5. **Create a new DataFrame** that computes **Debt-to-Income ratio** for every business  
   - Debt-to-Income = `Total Long-term Debt / Total Revenue`
6. **Concatenate (merge) the Debt-to-Income DataFrame** back into the original DataFrame

---

## Dataset

**File:** `D598 Data Set.xlsx`

### Expected Columns
- `Business ID`
- `Business State`
- `Total Long-term Debt`
- `Total Equity`
- `Debt to Equity`
- `Total Liabilities`
- `Total Revenue`
- `Profit Margin`

---

## Outputs Produced

After running the script/notebook, the following DataFrames are created:

- `duplicates_df`  
  Duplicate rows in the dataset (full-row duplicates).

- `ids_by_state_df`  
  List of **Business IDs grouped by Business State** (helpful for validating grouping logic).

- `stats_by_state_df`  
  State-level descriptive statistics (mean, median, min, max) for all numeric variables.

- `negative_dte_df`  
  Businesses where `Debt to Equity < 0`.

- `dti_df`  
  `Business ID` + computed `Debt to Income` ratio.

- `df_final`  
  Original dataset merged with the `Debt to Income` ratio column.

---

## How It Works (High-Level Flow)

1. Load Excel dataset into `df`
2. Detect duplicates → `duplicates_df`
3. Group by `Business State`:
   - IDs per state → `ids_by_state_df`
   - Stats per state → `stats_by_state_df`
4. Filter negative debt-to-equity → `negative_dte_df`
5. Compute debt-to-income ratio → `dti_df`
6. Merge ratio back into original dataset → `df_final`

---

## Running the Code

### Option A: Jupyter Notebook
1. Open terminal and navigate to your project folder:
   ```bash
   cd /path/to/your/project
jupyter lab
Open your notebook and run all cells.
