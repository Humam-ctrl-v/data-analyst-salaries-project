{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "002ddc25-bfb4-4ea6-8b60-814c9022d892",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "id": "bb9f6039-ffc0-45be-9773-515677872f59",
   "metadata": {},
   "source": [
    "# ✅ Checkpoint 1: Data Cleaning and Preparation (Step 1 Completed)\n",
    "\n",
    "## 📁 Dataset: San Francisco City Employee Salaries - 2011  \n",
    "*File used: `salaries_cp.csv` (copy of raw data)*\n",
    "\n",
    "---\n",
    "\n",
    "## 🛠️ Step 1: Data Inspection & Cleaning\n",
    "\n",
    "This checkpoint covers the full completion of the initial step in the data analysis pipeline. Below is a breakdown of what has been done:\n",
    "\n",
    "### 🔍 1. Column Inspection & Data Types\n",
    "- Inspected all 14 columns for data types, inconsistencies, and potential cleaning needs.\n",
    "- Noted that:\n",
    "  - `Agency` and `Year` each contained only one unique value (`San Francisco`, `2011`).\n",
    "  - Several columns contained `NaN` values or were entirely empty.\n",
    "\n",
    "**Action:** Decidede to delete both Agency and Year columns for their lack of analytical value from the copy am working on ( the original data won`t be altered.\n",
    "---\n",
    "\n",
    "### 🧹 2. Dropped Useless Columns\n",
    "- Identified and removed columns that were entirely or mostly filled with `NaN` values and had no analytical significance.\n",
    "\n",
    "---\n",
    "\n",
    "### 🧼 3. Handled Missing Values\n",
    "- Filled missing values in `BasePay`, `OvertimePay`, and `OtherPay` with `0`, assuming no pay in absence of data.\n",
    "- Reconstructed the `TotalPay` column using the following formula:\n",
    "\n",
    "```python\n",
    "df['TotalPay'] = df['BasePay'] + df['OvertimePay'] + df['OtherPay']\n",
    "- Also creating ComputedTotalPay  columns to compare it with TotalPay column incase if any value would not be equal it will be flagged and resolved\n",
    "- Ensured each column will have its respected data type (numerical only since i will be doing some statistics on the string columns next)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "34e384f3-5cf6-482e-9eeb-1665b58ecb20",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python [conda env:base] *",
   "language": "python",
   "name": "conda-base-py"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.7"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
