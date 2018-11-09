
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
On Linux/Mac, start bin/bigtangle-server. 
On Windows,	use bin\bigtangle-server.bat to start the server application.