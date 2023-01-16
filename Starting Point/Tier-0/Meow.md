# Meow  

## Task 1  
Q: What does the acronym VM stand for?  
A: virtual machine  

## Task 2  
Q: What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.  
A: terminal  

## Task 3  
Q: What service do we use to form our VPN connection into HTB labs?  
A: openvpn  

## Task 4  
Q: What is the abbreviated name for a 'tunnel interface' in the output of your VPN boot-up sequence output?  
A: tun  

## Task 5  
Q: What tool do we use to test our connection to the target with an ICMP echo request?  
A: ping  

## Task 6  
Q: What is the name of the most common tool for finding open ports on a target?  
A: nmap  

## Task 7  
Q: What service do we identify on port 23/tcp during our scans?  
A: telnet  

## Task 8  
Q: What username is able to log into the target over telnet with a blank password?  
A: root  

## SUBMIT FLAG  
``` text
1. scan open ports.
    (1) [host] # nmap -sV ${ip}
2. telnet to target.
    (1) [host] # telnet ${ip}
    (2) enter "root" without password to login.
3. find flag.
    (1) [root@Meow]:~# ls
    (2) [root@Meow]:~# cat flag.txt
```
A: b40abdfe23665f766f9c61ecba8a4c19