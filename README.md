# Applying ETL process to WashingtonPost Killing database
Python code to apply ETL process on Washington Post Killings database and linking to US Census files.
Following is the summary of process followed:

1. Extract washington post & Census data from csv files to pandas dataframes. We used 'chardet' module to guess detection of character encoding in a few csv files, as default utf-8 was not working. 

2. Transform the data 
<ul>
    <li>Address missing data and data type issues. </li>
    <li>Making sure that City Name field has common format  washington post data and US Census data files. It needed some data      transformation. City names is used as common key to join the dataframes. </li>
    <li>Use web API's from NamSor.com to guess race of persons (missing for a few records in washington post database).</li>
 </ul>
3. Load final pandas dataframe to MySQL database using 'sqlalchemy' module.

Complete code is available in repository.
