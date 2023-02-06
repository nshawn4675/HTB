# Sequel  

# Task 1  
Q: During our scan, which port do we find serving MySQL?  
A: 3306  

# Task 2  
Q: What community-developed MySQL version is the target running?  
A: MariaDB  

# Task 3  
Q: When using the MySQL command line client, what switch do we need to use in order to specify a login username?  
A: -u  

# Task 4  
Q: Which username allows us to log into this MariaDB instance without providing a password?  
A: root  

# Task 5  
Q: In SQL, what symbol can we use to specify within the query that we want to display everything inside a table?  
A: *  

# Task 6  
Q: In SQL, what symbol do we need to end each query with?  
A: ;  

# Task 7  
Q: There are three databases in this MySQL instance that are common across all MySQL instances. What is the name of the fourth that's unique to this host?  
A: htb  

# SUBMIT FLAG  
``` text
1. scan open ports
    (1) [host] # nmap -sC -sV ${ip} -v
2. try to connect to service without password.
    (1) [host] # mysql -h ${ip} -u root
3. find flag in sql service.
    (1) MariaDB [(none)]> SHOW databases;
    (2) MariaDB [(none)]> USE htb;
    (3) MariaDB [htb]> SHOW tables;
    (4) MariaDB [htb]> select * from config;
```
A: 7b4bec00d1a39e3dd4e021ec3d915da8