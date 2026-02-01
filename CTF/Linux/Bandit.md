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



