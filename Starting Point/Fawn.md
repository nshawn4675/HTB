# Fawn  

## Task 1  
Q: What does the 3-letter acronym FTP stand for?  
A: file transfer protocol  

## Task 2  
Q: Which port does the FTP service listen on usually?  
A: 21  

## Task 3  
Q: What acronym is used for the secure version of FTP?  
A: sftp  

## Task 4  
Q: What is the command we can use to send an ICMP echo request to test our connection to the target?  
A: ping  

## Task 5  
Q: From your scans, what version is FTP running on the target?  
A: unix  

## Task 6  
Q: What is the command we need to run in order to display the 'ftp' client help menu?  
A: ftp -h  

## Task 7  
Q: What is the command we need to run in order to display the 'ftp' client help menu?  
A: ftp -h  

## Task 8  
Q: What is username that is used over FTP when you want to log in without having an account?  
A: anonymous  

## Task 9  
Q: What is the response code we get for the FTP message 'Login successful'?  
A: 230  

## Task 11  
Q: What is the command used to download the file we found on the FTP server?  
A: get  

## SUBMIT FLAG  
``` text
1. scan open ports.
    (1) [host] # nmap -sV ${ip}
2. ftp to target.
    (1) [host] # ftp ${ip}
    (2) enter "anonymous" as username and any password.
3. get flag.txt
    (1) ftp> ls
    (2) ftp> get flag.txt
    (3) ftp> exit
    (4) [host] # cat flag.txt
```
A: 035db21c881520061c53e0536e44f815