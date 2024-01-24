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
**SSH-** The Secure Shell (SSH) protocol is a method for securely sending commands to a computer over an unsecured network. SSH uses cryptography to authenticate and encrypt connections between devices.

#### Solution
The SSH command is used to enter the level zero.
Given : 
     host name: bandit.labs.overthewire.org
     port: 2220
     username: bandit0
     password: bandit0
Type:
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

![image](https://github.com/Shanu48/Bandit/assets/149718849/e6acbc3d-30b2-44f9-88a9-6764a71c39b0)

Enter the givenn password: bandit0

** Note ** - Bandit does not show you the password while typing nor does it move the coursor.

To enter into a level you need to exit the previous one with the help of ```exit -d``` command.
