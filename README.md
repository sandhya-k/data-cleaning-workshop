# Data Cleaning Workshop
When: March 20,2019

Where: IRE Chicago meetup

Note: This class is adapted from the [Investigative Reporters and Editors](https://www.ire.org/) CARwash class and includes some of the instructions they've shared for the class.

----
Description: Dirty data lurk everywhere. We'll walk through some integrity checks to help diagnose problems with your data and learn how to deal with some of the most common problems, including standardizing misspelled names. 

This session is good for: People with some experience working with data in columns and rows, in spreadsheets or database managers.

Objectives: Practice using a typical data cleaning workflow in Excel, including filtering and pivoting to perform integrity checks to find misspellings, nonstandard values, etc.

Data for this workshop is here: [http://bit.ly/2OkpjM8](http://bit.ly/2OkpjM8)

- `data-cleaning-IRE` -- we'll be using a spreadsheet that I've made with lots of data problems
- `ildebtor.xslx` -- Child support orders from Illinois

Data cleaning steps for the `data-cleaning-IRE` file:
- Look at the `example-dirty-data`. Look at the dates, dollar amounts, city names. What is wrong with this worksheet? 
- Example header worksheet is `dirty-data-headers`.
- Let's talk about colors! See the `example-color` worksheet.
- What about dates? See the `dates-cleaning` worksheet for the different ways dates can be formatted. 
Note: Sometimes the messiness is very subtle! This data serves as an example of some of the many things that can go wrong in your data. 

Data cleaning steps for the `ildebtor` file:
1.  Make a copy of the original file and leave the data untouched. Keep this file as a reference. Create a data diary and a data dictionary. A data diary is a record of every step you've taken to clean the data and analyze it. The data dictionary is a reference file which will explain what the headers mean, along with any codes. This will be helpful in recreating your work. 
2. Create a pivot table to group by city to find misspellings. Run integrity checks on any text field that will be part of your analysis. Filters can also be a way to get a quick read of data cleanliness, which is useful when estimating the time needed to clean and analyze a data set.
3. Create a new clean_city column, and copy+paste the city column into it. Filter to find Chicago misspellings, fix manually (bulk find-replace). Look for other cities too. [Open Refine](http://openrefine.org/download.html) can also come in handy for cleaning names or addresses in bulk.  
4. Do a similar pivot table to find similar names and addresses. What do you see? Names and addresses are some of the dirtiest data. 
5. Sort on numeric and date columns to check for outliers. What are the minimum and maximum values? Summarize the data (sum, mean, mode,median). Are there negative values? Are there NAs? Are there blanks? 

---
Some useful resources: 
- [Structuring your data](https://source.opennews.org/articles/building-cleaner-smarter-spreadsheets/)
- [Mary Jo Webster's Excel Magic file](https://mjwebster.github.io/DataJ/tipsheets/ExcelMagic.pdf)
- [Quartz Guide to Bad Data](https://github.com/Quartz/bad-data-guide)