
# Install mysql database

# create database for Bigtangle
``` 
CREATE DATABASE info  character set utf8 COLLATE utf8_general_ci;
USE info;
CREATE USER 'info'@'%' IDENTIFIED BY 'info';
REVOKE ALL PRIVILEGES, GRANT OPTION FROM 'info'@'%';
GRANT SELECT,INSERT,UPDATE,DELETE,LOCK TABLES,EXECUTE ON info.* TO 'info'@'%';
FLUSH PRIVILEGES;

```

# download the Bigtangle server
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

The you can check the log  file.