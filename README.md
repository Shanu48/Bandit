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

** Note ** - Bandit does not show you the password while typing nor does it move the cursor.

To enter into a level you need to exit the previous one with the help of ```exit -d``` command.

---
## Level 0 -> Level 1
#### Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

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
The password for the next level is stored in the file data.txt next to the word millionth

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: Lets open the file
```
cat data.txt
```

Step 3: Its a huge file so it will take a long time to search. 

Its given that, the password is stored next to the word "millionth"
```
grep "millionth" "data.txt"
```

Here's the password. Copy or store it somewhere to use later
```
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

---
## Level 8 -> Level 9
#### Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

#### Solution

Step 1: Lets first check all the files that are available
```
ls
```

Step 2: This is a huge file. 

Its given that the password is the file that occurs only ones. 

So, we need to remove the repeating lines. First we need to sort the lines and then find the unique line
```
cat data.txt | sort | uniq
```

Here's the password. Copy or store it somewhere to use later
```
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

---
## Level 9 -> Level 10
#### Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

#### Solution

The password is in a human readable file preceded by ```=``` characters

Its mostly binary. We need only strings preceded by ```=```

Lets open the file
```
strings data.txt | grep "="
```
![image](https://github.com/Shanu48/Bandit/assets/149718849/d64b0d81-6b6f-40f3-8d40-fe43d09f08c3)

Our password is the string preceded by lots of ```=```

Here's the password. Copy or store it somewhere to use later
```
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

---
## Level 10 -> Level 11
#### Level Goal
The password for the next level is stored in the file data.txt, which contains base64 encoded data

#### Solution

The file has base64 encoder. Let decode it and open the file
```
cat data.txt | base64 --decode
```

Here's the password. Copy or store it somewhere to use later
```
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```

---
## Level 11 -> Level 12
#### Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

#### Solution

This is the command to rotate a string my 13 positions
```
cat data.txt | tr 'a-z' 'n-za-m' | tr 'A-Z' 'N-ZA-M'
```

But, our srting is already rotated. We need it back
```
cat data.txt | tr 'n-za-m' 'a-z' | tr 'N-ZA-M' 'A-Z'
```

Here's the password. Copy or store it somewhere to use later
```
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```

---
## Level 12 -> Level 13
#### Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

#### Solution

The file has been compressed multiple times. It had been suggested that we decompress is while putting it in a new file.

Step 1: Lets make a folder named tmp and in it lv12
```
mkdir /tmp/lv12
```

Step 2: Lets copy data.txt in this newly created folder
```
cp data.txt /tmp/lv12
```

Step 3: Get into this floder
```
cd /tmp/lv12
```

To check the type or encoding of the file use ```file <filename>``` command

Step 4: ```data.txt``` is a hex file so we need to convert it
```
xxd -r data.txt >data
```


Frequently check the type and compression of the newly created file to know the next step


**For a gzip file:**

1. Create a file with .gz extention ```mv <oldfilename> <newfilename>.gz```

2. To unzip it ```gzip -d <newfilename>.gz```

3. New file can be seen ```newfilename```


**For a bzip2 file:**

1. Create a new file with .bz extention ```mv <newfilename> <newfilename2>.bz```

2. Open it using ```bzip2 -d <newfilename2>.bz```

3. Info about a new data file will be given. This is a .bin file

4. Create a new file using .gz


**For a gzip .bin file:**

1. Use ```gzip -d <newfilename>.gz```

2. Its file type now is ```tar```

3. Create a new file using .tar

4. Open it using ```tar -xf <newfilename>.tar```

5. It will create a .bin file

6. Move it to a new .tar file

7. Open it accordingly



Stop once the file type is ```ASCII text```

Here lies the password
```
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

---
## Level 13 -> Level 14
#### Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

#### Solution

We need to enter bandit14 through bandit13
```
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

Its told that the password is in ```/etc/bandit_pass/bandit14```

Lets open it up
```
cat /etc/bandit_pass/bandit14
```

Here's the password. Copy or store it somewhere to use later
```
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```

---
## Level 14 -> Level 15
#### Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

#### Solution
We need to connect to the localhost 30000 and prompt the shell using the password retrived in previous level
```
nc localhost 30000
```
Press enter and provide the password obtained in the previous level

Here's the password. Copy or store it somewhere to use later
```
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```

---
## Level 15 -> Level 16
#### Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

#### Solution
OpenSSL is a library for secure communication over networks. It implements the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) cryptographic protocols that are, for example, used in HTTPS to secure the web traffic.

openssl s_client is the implementation of a simple client that connects to a server using SSL/TLS.

We need ssl encryption
```
openssl s_client -connect localhost:30001
```

Press enter and provide the password obtained in the previous level

Here's the password. Copy or store it somewhere to use later
```
JQttfApK4SeyHwDlI9SXGR50qclOAil1
```

---
## Level 16 -> Level 17
#### Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

#### Solution
Find out which port is listening
```
nmap localhost -p31000-32000

```
We have only these 5. Open them one by one. One of them will give you the ```RSA PRIVATE KEY```
```
Starting Nmap 7.80 ( https://nmap.org ) at 2024-02-05 13:56 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00014s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown
```
Its port ```31790```

We need to store this private key somewhere. Bandit won't allow us to create a new file. So lets store it in the tmp file.
```
mkdir /tmp/private
```

The folder has been created. Now lets create a file to store the key. The ```.key``` is important here.
```
touch private.key
```

Now copy the private key. We have to paste it in ```private.key```. We can't use ```cat``` here because its for appending the data. Once we exit we won't be able to access the data. 
```
vim private.key
```
```vim``` is a text editor. It's used to read contents to the file. 

Now press ```i``` to enter the insert mode and paste the private key. 

To exit without saving press ```esc``` key and type ```:qa!```

To save the content and exit press ```esc``` and type ```:wq```

Now we need to open ```bandit17``` using this private key
```
ssh -i private.key bandit17@bandit.labs.overthewire.org -p 2220
```
We are in!!!

But we might need the password for future. Every password is stored in ```/etc/bandit_pass/bandit<level_no>```. Access it using ```cat```

Here's the password. Copy or store it somewhere to use later
```
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```

---
## Level 17 -> Level 18
#### Level Goal
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

#### Solution

We simply need to find the one line that is different in both the files
```
diff passwords.new passwords.old
```

Here's the password. Copy or store it somewhere to use later
```
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```

---
## Level 18 -> Level 19
#### Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

#### Solution

This time, the terminal won't allow us to enter. We need to force it to give us the info we need.

Let's check what files we have.
```
ssh bandit18@bandit.labs.overthewire.org -p 2220 **ls**
```

Now let's open ```readme``` as usual
```
ssh bandit18@bandit.labs.overthewire.org -p 2220 **cat readme**
```

Here's the password. Copy or store it somewhere to use later
```
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```

---
## Level 19 -> Level 20
#### Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 20 -> Level 21
#### Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 21 -> Level 22
#### Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 22 -> Level 23
#### Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 23 -> Level 24
#### Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 24 -> Level 25
#### Level Goal
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 25 -> Level 26
#### Level Goal
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 26 -> Level 27
#### Level Goal
Good job getting a shell! Now hurry and grab the password for bandit27!

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 27 -> Level 28
#### Level Goal
There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

Clone the repository and find the password for the next level.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 28 -> Level 29
#### Level Goal
There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

Clone the repository and find the password for the next level.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 29 -> Level 30
#### Level Goal
There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

Clone the repository and find the password for the next level.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 30 -> Level 31
#### Level Goal
There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.

Clone the repository and find the password for the next level.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 31 -> Level 32
#### Level Goal
There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.

Clone the repository and find the password for the next level.

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 32 -> Level 33
#### Level Goal
After all this git stuff its time for another escape. Good luck!

#### Solution

Here's the password. Copy or store it somewhere to use later
```

```

---
## Level 33 -> Level 34
#### Level Goal
At this moment, level 34 does not exist yet.
