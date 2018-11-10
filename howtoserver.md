
# Install mysql database

# Create database for Bigtangle
``` 
ALTER USER 'root'@'localhost' IDENTIFIED BY 'test1234';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'test1234' WITH GRANT OPTION;
CREATE DATABASE info  character set utf8 COLLATE utf8_general_ci;

```
# Import the database file from daily backup testnet
 [Download database](https://github.com/bigtangle/zipfile/blob/master/bigtangle-database.sql)
 Then import this sql file
 mysql -u root -ptest1234  info < bigtangle-database.sql
 

# Download the Bigtangle server
 [Download](https://github.com/bigtangle/zipfile/blob/master/bigtangle-server.zip)
 
# Start Server
Unzip the file bigtangle-server.zip.

On Linux/Mac,

export SERVER_PORT=8088  
export DB_NAME=info 
export DB_PASSWORD=test1234 
export DB_HOSTNAME=localhost
export SERVICE_MILESTONE_RATE=50000 
export SERVICE_MILESTONE_ACTIVE=true 
export SERVER_MINERADDRESS=mwSU7SDr5gQjRktYvz5wzA9ef3kGgGnHHN  
export BOOT_STRAP_SERVERS=de.kafka.bigtangle.net:9092 
export CONSUMERIDSUFFIX=mwSU7SDr5gQjRktYvz5wzA9ef3kGgGnHHN
export REQUESTER=https://bigtangle.org, https://bigtangle.de  

 start bin/bigtangle-server.

 
On Windows,	open cosole

set SERVER_PORT=8088  
set DB_NAME=info 
set DB_PASSWORD=test1234 
set DB_HOSTNAME=localhost
set SERVICE_MILESTONE_RATE=50000 
set SERVICE_MILESTONE_ACTIVE=true 
set SERVER_MINERADDRESS=mwSU7SDr5gQjRktYvz5wzA9ef3kGgGnHHN  
set BOOT_STRAP_SERVERS=de.kafka.bigtangle.net:9092 
set CONSUMERIDSUFFIX=mwSU7SDr5gQjRktYvz5wzA9ef3kGgGnHHN
set REQUESTER=https://bigtangle.org, https://bigtangle.de  

use bin\bigtangle-server.bat to start the server application.

Then you can check the log file.