# Redeemer  

## Task 1  
Q: Which TCP port is open on the machine?  
A: 6379  

## Task 2  
Q: Which service is running on the port that is open on the machine?  
A: redis  

## Task 3  
Q: What type of database is Redis? Choose from the following options: (i) In-memory Database, (ii) Traditional Database  
A: in-memory database  

## Task 4  
Q: Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments.  
A: redis-cli  

## Task 5  
Q: Which flag is used with the Redis command-line utility to specify the hostname?  
A: -h  

## Task 6  
Q: Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server?  
A: info  

## Task 7  
Q: What is the version of the Redis server being used on the target machine?  
A: 5.0.7  

## Task 8  
Q: Which command is used to select the desired database in Redis?  
A: select  

## Task 9  
Q: How many keys are present inside the database with index 0?  
A: 4  

## Task 10  
Q: Which command is used to obtain all the keys in a database?  
A: keys *  

## SUBMIT FLAG  
``` text
1. scan open ports
    (1) [host] # nmap -sV -p- ${ip}
    (it may take about 30 minutes)
2. connect to Redis server.
    (1) [host] # redis-cli -h ${ip}
3. find flag
    (1) ${ip}:6379> info
    (checkout # Keyspace)
    (2) ${ip}:6379> select 0
    (3) ${ip}:6379> keys *
    (4) ${ip}:6379> get flag
```
A: 