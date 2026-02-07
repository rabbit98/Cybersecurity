# BanditLabs

Open the [BanditLabs](https://banditlabs.com/) website.
## level 0
>Command 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
Explination : 
- p for port 
- ssh is secure shell
- bandit0 is the user
- bandit.labs.oberthewite.org is the host
>Password : 
```bash
bandit0
```

## level 0 to level 1
>Command 
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
ls
cat readme
```
Explination :
- ls is for list
- cat is for read
- readme is the file to be read from the list of files
>Password : 
```bash
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If  
```

## level 1 to level 2
>Command 
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
ls  
cat ./-
```
Explination :
- ls is for list
- cat is for read
- For - (Dash files) use ./(dot slash) command to check what is inside
- ./- is the file to be read from the list of files
>Password : 
```bash 
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
``` 

## level 2 to level 3
>Command  
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
ls  
cat ./--spaces\ in\ this\ filename--  
```
Explination :
- ls is for list
- cat is for read
- -found --spaces in this filename-- to open this use:
- ./--spaces\ in\ this\ filename-- is the file to be read from the list of files  
>Password : 
```bash     
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
``` 

## level 3 to level 4 
>Command 
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
ls  
cd inhere  
ls  
cat ./...Hiding-From-You  
```
Explination :
- ls is for list
- cat is for read
- cd is for change directory
- cd inhere to open this use:
- ./...Hiding-From-You is the file to be read from the list of files  
>Password : 
```bash     
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
``` 
## level 4 to level 5 
>Command 
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
ls  
find . -type f -exec file {} \; | grep ASCII ./-file07: ASCII text

bandit4@bandit:~/inhere$ find . -type f -exec file {} \; | grep ASCII | cut -d: -f1 | xargs cat
```
![alt text](image-1.png)

Explination :
- ls is for list
- cd is for change directory
- find . -type f -exec file {} \; | grep ASCII ./-file07: ASCII text to locate the file
- find . -type f -exec file {} \; | grep ASCII | cut -d: -f1 | xargs cat
- ./-file07 is the file to be read from the list of files
with the last command we can get the password present in the file 7 directly from the terminal
password : 
```bash     
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
## level 5 to level 6
>Command 
```bash    
ssh bandit6@bandit.labs.overthewire.org -p 2220
ls
find . -type f ! -executable -size 1033c -exec file {} \; | grep 'ASCII' | cut -d: -f1 | xargs cat
```
![alt text](image-2.png)

Explination :
- ls is for list
- cd is for change directory
- find inhere: Starts the search in the inhere directory.
- type f: Looks for regular files.
- ! -executable: Excludes executable files.
- size 1033c: Searches for files that are exactly 1033 bytes (c stands for bytes).
- exec file {} \;: For each file found, run the file command to determine its type (human-readable text).
- grep 'ASCII': Filters the files that are human-readable (ASCII text).
- cut -d: -f1: Extracts just the filenames from the file output.
- xargs cat: Passes the filenames to cat to display the contents of the file.

with the last command we can get the password present in the file 7 directly from the terminal

password : 
```bash
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
## level 6 to level 7
>Command 
```bash    
ssh bandit7@bandit.labs.overthewire.org -p 2220
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null -exec cat {} \;
```
![alt text](image-3.png)

Explination : 
- find / → search the entire filesystem
- type f → only regular files
- user bandit7 → owned by user bandit7
- group bandit6 → owned by group bandit6
- size 33c → exactly 33 bytes (c = bytes)
- 2>/dev/null → hides permission denied errors (important)
- exec cat {} \; → prints the file contents (the password)

password : 
```bash 
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
``` 
## level 7 to level 8
>Command 
```bash    
ssh bandit8@bandit.labs.overthewire.org -p 2220
grep millionth data.txt
```
![alt text](image-4.png)

Explination : 
- grep millionth data.txt → search for the millionth line in the data.txt file

password : 
```bash 
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
## level 8 to level 9
>Command 
```bash    
ssh bandit9@bandit.labs.overthewire.org -p 2220
sort data.txt | uniq -u
``` 
![alt text](image-5.png)

Explination : 
- sort data.txt → sort the data.txt file
- uniq -u → remove duplicate lines

password : 
```bash 
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
``` 
## level 9 to level 10
>Command 
```bash    
ssh bandit10@bandit.labs.overthewire.org -p 2220
strings data.txt | grep "^==="
```
![alt text](image-6.png)

Explination : 
- strings data.txt → extract strings from the data.txt file
- grep "^===" → search for lines that start with "==="

password : 
```bash 
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
``` 
## level 10 to level 11
>Command 
```bash    
ssh bandit11@bandit.labs.overthewire.org -p 2220  
base64 -d data.txt
```
![alt text](image-7.png)

Explination : 
- base64 -d data.txt → decode the base64 data.txt file
- -d for decode

password : 
```bash 
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
``` 
## level 11 to level 12
>Command 
```bash    
ssh bandit12@bandit.labs.overthewire.org -p 2220
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
![alt text](image-8.png)

Explination : 
- cat data.txt → read the data.txt file
- tr 'A-Za-z' 'N-ZA-Mn-za-m' → translate the characters A-Za-z to N-ZA-Mn-za-m

password : 
```bash 
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
``` 
## level 12 to level 13
>Command  
```bash    
ssh bandit13@bandit.labs.overthewire.org -p 2220
cd /tmp
mktemp -d
cd /tmp/tmp.ABC123xyz
cp ~/data.txt .
xxd -r data.txt > data
file data
data: gzip compressed data

mv data data.gz
gunzip data.gz

mv data data.bz2
bunzip2 data.bz2

mv data data.tar
tar -xf data.tar

cat data
```

Explination : 
- cd /tmp → change directory to /tmp
- mktemp -d → create a temporary directory
- cd /tmp/tmp.ABC123xyz → change directory to the temporary directory
- cp ~/data.txt . → copy the data.txt file to the temporary directory
- xxd -r data.txt > data → decode the data.txt file
- file data → identify the file type
- gzip → bzip2 → gzip → tar → gzip → tar → bzip2 → ASCII
- mv data data.gz → rename the data file to data.gz
- gunzip data.gz → decompress the data.gz file
- mv data data.bz2 → rename the data file to data.bz2
- bunzip2 data.bz2 → decompress the data.bz2 file
- mv data data.tar → rename the data file to data.tar
- tar -xf data.tar → extract the data.tar file
- cat data → read the data file
- repeat the steps until the password is found

![alt text](image-9.png)

password : 
```bash 
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
``` 
## level 13 to level 14
>Command 
```bash    
ssh bandit14@bandit.labs.overthewire.org -p 2220
scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private ~/
chmod 600 ~/sshkey.private
ls -l ~/sshkey.private  
ssh -i /home/kali/sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
cat /etc/bandit_pass/bandit14
``` 
Explination :
- 1st logged out from level 13
- use whoami to get the username then
- use scp to copy the private key to the current directory [-P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private ~/]
- use chmod to change the permissions of the private key to 600
- use ls to check the permissions of the private key
- use ssh to login to level 14 with the private key
- use cat to read the password

password : 
```bash 
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
## level 14 to level 15
>Command 
```bash 
nc localhost 30000  
cat /etc/bandit_pass/bandit14
```
Explination : 
- nc localhost 30000 → connect to localhost on port 30000
- it shows a blank screen then we have to type the password
![alt text](image-11.png)

password : 
```bash 
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo    
``` 
## level 15 to level 16
>Command 
```bash 
ssh bandit16@bandit.labs.overthewire.org -p 2220    
openssl s_client -connect localhost:30001
```
Explination : 
- ssh bandit16@bandit.labs.overthewire.org -p 2220 → login to level 16
- openssl s_client -connect localhost:30001 → connect to localhost on port 30001
- it shows a blank screen then we have to type the password
![alt text](image-12.png)

password : 
```bash 
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
## level 16 to level 17
>Command 
```bash 
ssh bandit17@bandit.labs.overthewire.org -p 2220
nmap -p 31000-32000 localhost : <port>
openssl s_client -connect localhost:31790
```
After getting the key from the ports we logged out from the bandit and used the kali to get into bandit 17

>Command 
```bash 
nano ~/bandit17.key
chmod 600 ~/bandit17.key
ls -l ~/bandit17.key
ssh -i ~/bandit17.key bandit17@bandit.labs.overthewire.org -p 2220
``` 
Explination :
- nmap is for network mapping
- -p is the ports to be scanned
- localhost is the host to be scanned
- <port> is the port to be scanned

 ![alt text](image-13.png)

- openssl s_client -connect localhost:31790 → connect to localhost on port 31790
- it shows a blank screen then we have to type the password 
- nano is for editing the file
- we will copy the key from the ports and paste it in the file [cnrl+o to save the file and cnrl+x to exit the nano editor]
- chmod is for changing the permissions of the file
- ls is for listing the file
- ssh is for secure shell
- -i is for identity file
- bandit17@bandit.labs.overthewire.org is the host
- 2220 is the port
- with this we are logging into bandit 17

password : 
```bash 
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```
## level 17 to level 18
>Command 
```bash 
ssh bandit18@bandit.labs.overthewire.org -p 2220

```

![alt text](image-14.png)
![alt text](image-15.png)







