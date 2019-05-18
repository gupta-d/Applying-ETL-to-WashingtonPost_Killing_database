# Applying ETL process to WashingtonPost Killing database
Apply ETL process on Washington Post Killings database and linking to US Census files

1. Read csv's using correct encoding method (guessing the encoding using 'chardet')
2. Address missing data and data type issues. Also making sure city name (that wd be used as a common key across tables) is consistent and available for all records
3. Using web API's from NamSor.com to guess race of persons (missing for a few records in washington post database)
4. Use 'sqlalchemy' to create MySQL database
