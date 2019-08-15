# Applying ETL process to WashingtonPost Killing database
Washington post keeps a detailed database of all US police killings. Intention of this project is to merge the relevant information from US Census datasets (city specific information where these incidents have taken place), and apply <b><u>Extract_Transform-Load (ETL)</u> </b>process to upload the data into standard MySQL database.

I have used pandas to extract the main data from csv file, apply required transformations to handle missing data, creating common key to join files and finally used sqlalchemy module to upload pandas dataframe in a MySQL database.  

Following is the high level summary summary of process followed:

1. <bExtract</b> washington post & Census data from csv files to pandas dataframes. I have used 'chardet' module to guess detection of character encoding in a few csv files, as default utf-8 was not working. 

2. <b>Transform</b> the data 
<ul>
    <li>Address missing data and data type issues. </li>
    <li>Making sure that City Name field has common format  washington post data and US Census data files. It needed some data      transformation. City names is used as common key to join the dataframes. </li>
    <li>Use <b>web API's from NamSor.com</b> to guess race of persons (missing for a few records in washington post database).</li>
 </ul>
3. <b>Load</b> final pandas dataframe to MySQL database using 'sqlalchemy' module.

Complete code is available in repository.
