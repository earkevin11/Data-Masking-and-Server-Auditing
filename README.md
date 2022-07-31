# Data-Masking-and-Server-Auditing

# What is Data Masking?
- This means taht data in the database table can be LIMITED for view to non-privileged users
- A rule can be created that can mask the data
- Based on the rule, you can decide on the amount of data to expose to the user


# Multiple Data Masking Rules
- Credit card masking rules - where we can mask the column that contains credit card details and only show the last four digits 
- Email - where only the first letter of the email address is exposed and the domain name of the email addresss is replaced with XXX.com
- Custom text - where you can decide which characters to expose for a field
- Random number - where you can generate a random number for the field

# How to enable Data Masking
- Select a table and column you want to mask
- Go to SQL databaser > select "Dynamic Data Masking" section > Add mask > select the schema > select the column 
- Select the masking field format you want and select save
- Create and sign into a non-privileged sql database user to check if the data masking worked. (query is on #251)



# Azure SQL Database Server Auditing
- Auditing for Azure SQL database feature can be used to track database events and write them to an audit log.
- This helps in regulatory compliance and helps to gain insights on any anomalies when it comes to database activities.
- Auditing can be enabled at the database or server level.
- If it is enabled at the server level, then it will be applied to all of the databases that reside on the server.


# How to enable the Auditing feature
- Create a LAW (we are going to ingest Azure SQL Database logs into the LAW)
- Azure SQL DB > Auditing > Select LAW > Save
- It will take 20-30 minutes to see data in the LAW. Be sure to perform activity in the Azure SQL DB.
- Users will be able to see SQL DB logins failed attempts and more.
