# AutoBudget

## Purpose
(This is a personal project that will be completed in time, school and other projects will take priority)

Automating budget tracking by importing csv files from the bank and visualizing reality against the planned budget. The goal is to simplify my current process of updating an Excel spreadsheet budget tracker by scanning my bank accounts to ensure bills have gone through, tagging/identifing major expenses, and relying on basic income/expense amounts to set long-term budgets.

## Design Plan
This project will use Python coding for UI and logic with an SQLite database for record keeping. 

### CSV Input
The basis for speeding up my process is to export the transaction records from my banks to a .csv file that will be read using Pandas. 

#### Make Universal
Since I'll make this public, in case anyone ever comes across it, the headers will need to be adjustable at the time of reading the .csv file since banks have different formats. If no export feature is available, the user could highlight, copy and paste into an Excel spreadsheet, saving it to .csv format and designating the columns by index.

#### Cash
Manual input of transactions need to be a capability for cash.

## User Interface
Use Custom_TKinter.

### Main Screen
Show the user their total balances (in accounts, in savings, in cash). Show the last time the budget was updated (using the input system). Show projected expenses (bills), estimated monthly expenses (averaged common expenses), and left over funds if any.

### Input Screen
Keeping it simple, load the .csv file, show a display of columns found and designate each column automatically but allow the user to redesignate. After pressing upload, give results of record counts added, ensure no duplicates are made, and update the database. Grouping like items will be tricky but important. For example, Amazon orders all have unique identifiers but all have Amazon in the name so these should all be grouped. The monthly Prime membership should be separated out and designated as a monthly recurring bill.

The key transaction types will be "Income: Taxable, Non-taxable, Other", "Expense: Recurring Bill, Standard Expense, Major Expense", and "Transfers: To savings, From savings, Other"
Then each will get various categories that the user can select and place certain expense labels in each. For example: "Electric bill, mortgage, gas, pets, groceries, eating out, recreation, etc."

### Details Screen
If the user has a common expense (say Harbor Freight in my case), show expense totals by location for a given time or details of how many records there are associated with that retailer.

## Later Features
Once the core of the program is flushed out, these are other features I intend to add to it. I have made some of these already in Excel but not very user friendly.

### Real Estate Tracking
Give an option to the user to add properties to track. Using webscrapping, pull the current market values from several different realty sites to get a rough, generalized market value. I want the user to also be able to add in their mortgage to see a side-by-side comparison. The mortgage part will need a little more effort to be able to calculate interest and how much has already been paid off versus left to pay. It would also be a good idea to see how much property taxes have change in previous years to give an average growth of that but it wouldn't be a very reliable value.

### Loan Planner
This will be a helpful tool for personal loans, mortages, student loans or auto loans. Essentially just a visualization of the prepayment of the loan with interest to get a good idea how long it will take and the overall cost of the loan (loan + interest).
