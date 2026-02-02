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
