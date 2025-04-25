Checkpoint 1: Data Cleaning and Preparation (Step 1 Completed)\n",
Dataset: San Francisco City Employee Salaries - 2011
*File used: salaries_cp.csv (copy of raw data)

Step 1: Data Inspection & Cleaning
This checkpoint covers the full completion of the initial step in the data analysis pipeline. Below is a breakdown of what has been done:

1. Column Inspection & Data Types
Inspected all 14 columns for data types, inconsistencies, and potential cleaning needs. Noted that:

Agency and Year each contained only one unique value (San Francisco, 2011).
Several columns contained NaN values or were entirely empty.
Action: Decidede to delete both Agency and Year columns for their lack of analytical value from the copy am working on ( the original data won`t be altered.

2. Dropped Useless Columns
Identified and removed columns that were entirely or mostly filled with NaN values and had no analytical significance.
3. Handled Missing Values
Filled missing values in BasePay, OvertimePay, and OtherPay with 0, assuming no pay in absence of data.
Reconstructed the TotalPay column using the following formula:
        df['TotalPay'] = df['BasePay'] + df['OvertimePay'] + df['OtherPay']
        
- Also creating ComputedTotalPay  columns to compare it with TotalPay column incase if any value would not be equal it will be flagged and resolved
- Ensured each column will have its respected data type (numerical only since i will be doing some statistics on the string columns next)
