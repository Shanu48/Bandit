---
 # Bandit

 
This repo consists of data and steps required to solve Bandit problems.

---

## What is OverTheWire Bandit?
The Bandit wargame from OverTheWire is aimed at absolute beginners. It is a game you connect to through SSH that will help you will improve your command line skills, your linux skills, and you hacker skills.

---

## Aim
The aim of the game is to use various commands and obtain the password to enter the next level.

---

## Level 0
#### Level goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

#### Commands required
```**SSH-**``` The Secure Shell (SSH) protocol is a method for securely sending commands to a computer over an unsecured network. SSH uses cryptography to authenticate and encrypt connections between devices.

#### Solution
The SSH command is used to enter the level zero.
Given : 
     host name: bandit.labs.overthewire.org
     port: 2220
     username: bandit0
     password: bandit0
Step 1:
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

![image](https://github.com/Shanu48/Bandit/assets/149718849/e6acbc3d-30b2-44f9-88a9-6764a71c39b0)

Enter the givenn password: bandit0

** Note ** - Bandit does not show you the password while typing nor does it move the coursor.

To enter into a level you need to exit the previous one with the help of ```exit -d``` command.

---
## Level 0 -> Level 1
#### Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

#### Commands Required
```ls```
```cat```

#### Solution
We need to open a file called ```readme``` which is located in a directory called ```home```

Step 1: Lets first check all the files that are available
```
ls
```

![image](https://github.com/Shanu48/Bandit/assets/149718849/f2cdcd5d-1959-4a01-8933-8e47f59eac68)

Step 2: Lets open the file
```
cat readme
```

![image](https://github.com/Shanu48/Bandit/assets/149718849/11ddce42-3ab1-4f09-b18d-b1b815daf93c)

Here's the password. Copy or store it somewhere to use later
```
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```

---
## Level 1 -> Level 2
#### Level Goal
The password for the next level is stored in a file called - located in the home directory

#### Commands Required
ls
cat ./<filename>
#### Solution
Since the file name is ```-```, it con't be opened directly with the ```cat``` command
Step 1: Lets first check all the files that are available
```
ls
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/5c825a0a-0c61-48b2-81bb-781996a58018)

Step 2: Lets open the file
```
cat ./-
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/a9066d03-cb1b-49d5-b459-0dcbc7e13893)

Here's the password. Copy or store it somewhere to use later
```
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

---
## Level 2 -> Level 3
#### Level Goal
The password for the next level is stored in a file called spaces in this filename located in the home directory

#### Commands Required
ls
cat ./"<File name>
#### Solution
Step 1: Lets first check all the files that are available
```
ls
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/a3acc61a-564c-4393-ac30-c06eb4c592b3)

Step 2: Lets open the file. This time, the file name is not a single word. Hence, we need to type the name with quatations.
```
cat ./"spaces in the filename"
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/10775d2e-5ee7-4c8b-80dd-b69a4d62b7cc)

Here's the password. Copy or store it somewhere to use later
```
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

If the name of the file is written without the quotations, the terminal considers each word as a separate file.
![image](https://github.com/Shanu48/Bandit/assets/149718849/e75ad9d1-56ac-4bb4-afe6-33396a6bbf9e)

---
## Level 3 -> Level 4
#### Level Goal
The password for the next level is stored in a hidden file in the inhere directory.

#### Commands Required
ls
cd
dir -a
#### Solution
Step 1: Lets first check all the files that are available
```
ls
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/7592a3fe-d3e5-481a-9b9c-9e6c8cdf9af9)

Step 2: This time we have a directory ```inhere```. Lets open it
```
ch inhere
```

Step  3: Now, lets see what is inside ```inhere```
```
dir -a
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/ac62e1aa-2c5a-4f3b-8901-a07aa0ac4f4a)

We now have a file named ```.hidden```

Step 4: Let's open it up
```
cat .hidden
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/e39f3c72-4ec8-4701-98c5-c23209625142)

Here's the password. Copy or store it somewhere to use later
```
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```

---
## Level 4 -> Level 5
#### Level Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

#### Commands Required

#### Solution
Step 1: Lets first check all the files or directories that are available
```
ls
```

Step 2: There are multiple files here. The open that we can read consists of the passwords. Lets open them one by one
![image](https://github.com/Shanu48/Bandit/assets/149718849/046feded-64ac-4b72-89a8-8d411bd64d56)

Here's the password. Copy or store it somewhere to use later
```
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

---
## Level 5 -> Level 6
#### Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Inside ```inhere``` there are multiple other directories. Lets give a command so that the prompt will find the required file for us.
```
find -readable -size 1033c
```

Step 3: Now let's open the ```file2``` in ```maybehere07``` directory
```
cat ./maybehere07/.file2
```

![image](https://github.com/Shanu48/Bandit/assets/149718849/1026cfa9-357d-490f-8bee-9054cf1b2c07)

Here's the password. Copy or store it somewhere to use later
```
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

---
## Level 6 -> Level 7
#### Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

#### Commands Required

#### Solution

Step 1: This time we have to find a file that is on the server.
```
find / -user bandit7 -group bandit6 -size 33c
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/60190d38-3d62-4d63-8bf4-bf95e5ac1bc4)

We can see multiple files, but they all have permission denied

Step 2: Lets get rid of that
```
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

Step 3: Lets open up the file
```
cat /var/lib/dpkg/info/bandit7.password
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/76cababd-f9ae-4635-8f73-c3acd716c734)

Here's the password. Copy or store it somewhere to use later
```
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

---
## Level 7 -> Level 8
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level  -> Level 
#### Level Goal

#### Commands Required

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```

```

Here's the password. Copy or store it somewhere to use later
```

```
