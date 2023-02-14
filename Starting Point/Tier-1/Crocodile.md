# Crocodile  

## Task 1  
Q: What Nmap scanning switch employs the use of default scripts during a scan?  
A: -sC  

## Task 2  
Q: What service version is found to be running on port 21?  
A: vsftpd 3.0.3  

## Task 3  
Q: What FTP code is returned to us for the "Anonymous FTP login allowed" message?  
A: 230  

## Task 4  
Q: After connecting to the FTP server using the ftp client, what username do we provide when prompted to log in anonymously?  
A: anonymous  

## Task 5  
Q: After connecting to the FTP server anonymously, what command can we use to download the files we find on the FTP server?  
A: get  

## Task 6  
Q: What is one of the higher-privilege sounding usernames in 'allowed.userlist' that we download from the FTP server?  
A: admin  

## Task 7  
Q: What version of Apache HTTP Server is running on the target host?  
A: Apache httpd 2.4.41  

## Task 8  
Q: What switch can we use with Gobuster to specify we are looking for specific filetypes?  
A: -x  

## Task 9  
Q: Which PHP file can we identify with directory brute force that will provide the opportunity to authenticate to the web service?  
A: login.php  

## SUBMIT FLAG  
``` text
1. scan open ports
    (1) [host] # nmap -sC -sV ${ip} -v
2. try to access FTP server anonymously
    (1) [host] # ftp ${ip}
    (2) enter 'anonymous' as username
3. get account info from FTP server
    (1) ftp> ls
    (2) ftp> get allowed.userlist
    (3) ftp> get allowed.userlist.passwd
    (4) ftp> exit
4. check the website which the target hosts.
    (1) Use a browser to visit http://${ip}/
    (2) Can use 'Wappalyzer' to check the techniques used on the website.
5. gobuster the website
    (1) [host] gobuster dir --url http://${ip}/ --wordlist /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -x php,html
    (2) found /login.php
6. get the flag
    (1) Use a browser to visit http://${ip}/login.php
    (2) enter admin:rKXM59ESxesUFHAd as account info.
```
A: c7110277ac44d78b6a9fff2232434d16  
