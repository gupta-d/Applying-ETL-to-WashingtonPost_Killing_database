# Applying-ETL-to-WashingtonPost_Killing_database
Apply ETL process on Washington Post Killings database and linking to US Census files

1. Read csv's using correct encoding method (guessing the encoding using 'chardet)
2. Address data formatting, missing data and data types issues. Also making sure city name (that wd be used as a common key across tables) is consistent and available for all records
3. using web API's from NamSor to guess race of persons that were missing for a few records
4. use 'sqlalchemy' to create MySQL database
