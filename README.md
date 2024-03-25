# Data Cleaning

## Introduction
Data cleaning is an essential stage in the data analysis pipeline, crucial for ensuring accuracy and reliability in decision-making processes. In this documentation, I outline a comprehensive data cleaning process undertaken using Microsoft Excel. The objective was to transform raw data into a standardized and organized format suitable for analysis. Through a series of systematic steps, various issues such as inconsistent formatting, erroneous entries, and structural anomalies were identified and rectified. This documentation provides a detailed account of the procedures employed, ranging from simple formatting adjustments to complex formula implementations. By documenting this process, not only can future analysts understand the transformations applied to the dataset, but it also ensures transparency and reproducibility in data manipulation tasks. Let's delve into the intricacies of each step taken to refine the dataset and prepare it for analysis. :smile:

### Problems I observed in the dataset that required attention during the data cleaning process;
- Inconsistent column width and row height, affecting readability.
- Lengthy client names with additional characters in parentheses, making them difficult to manage.
- Inconsistent formatting and spacing in the contact column.
- Department and region information combined in a single column separated by '_', making it challenging to analyze.
- Presence of duplicate entries within the dataset.
- Blank cells present in the payment column.
- Errors in the profit margin column due to text entries mixed with numeric values.
- Redundant headers or irrelevant data in the first row and column.

  ### Solution
1. Autofitting Columns and Rows.
- Utilized autofit to adjust columns and rows for better readability.
    Shortcut: Alt + H + O + I for columns and Alt + H + O + A for rows.
  
2. Client Column Adjustment.
- Identified long names with additional characters in parentheses in the client column.
- Utilized the Find and Replace function (Ctrl + H) to shorten names and remove additional characters.
Find: (*)
Replace with: Nothing. NB: don't type 'nothing' I mean leave it blank
- Created a new column named "client" to convert names to lowercase using the LOWER function.
- Replaced the old client column with the new one:Select new client column using Ctrl + Shift + Down Arrow.
Copied (Ctrl + C) and pasted as values.
- Deleted the previous client column.

3. Contact Column Standardization.
- Observed spacing and inconsistent capitalization in the contact column.
- Created a new column and applied the TRIM and PROPER functions to standardize entries.
Formula: =TRIM(PROPER(D3))
- Filled the entire column by double-clicking the corner of the cell.
- Deleted the previous contact column.

4. Department and Region Separation
- Noticed that the department and region were combined with '_' as a separator.
- Created a new column named "region" to separate them.
- Used the Text to Columns feature under the Data tab, selecting '_' as the delimiter.

5. Removing Duplicates
- Checked for duplicates and removed them using the Remove Duplicates function under the Data tab.

6. Handling Blank Cells in Payment Column
- Selected the entire table and identified blank cells in the payment column.
- Used the Go To Special function (Home > Find and Select > Go To Special > Blanks) to select blank cells.
- Entered "N/A" into selected blank cells and filled them using Ctrl + Enter.

7. Addressing Errors in Profit Margin Column
- Noticed errors in the profit margin column due to text entries.
- Implemented the IFERROR function to handle errors.
Formula: =IFERROR(H2/G2,"N/A")
- Applied the formula to the entire column.

8. Formatting Headers and Cleaning
- Deleted the first row and column if they contained no relevant data.
- Formatted headers by boldening, changing background colors, and adjusting font colors.

  And Voila, we are done, ta-daa! 🏃🤎😄 . Find the dirty and clean data [here](https://1drv.ms/x/c/edec0aad78d7cfca/ESFz7JlJXxBHr8VbZfLoXxEBXSZbBPjnHQSZEEjOt5dR3A?e=tyNHaB)


   
