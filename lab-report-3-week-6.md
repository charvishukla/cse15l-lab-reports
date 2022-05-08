# CSE 15L Lab 3

> __Name__ : Charvi Shukla 

> __Email__ : cshukla@ucsd.edu 

## Introduction
Hello! Welcome to my Lab Report 3 - Week 6 for CSE 15L!
In this lab report I will be going over the following:
* Streamlining `ssh` configuration 
* Setting up Github Access from ieng6
* Copying whole directories with scp -r

## Task 1: Streamlining `ssh` Configuration 

**Step 1**
For the first step, I created a folder called `ssh` and created a `config` file inside it. 
Then, in Visual Studio Code, I added the following lines into the `config` file:

```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22adl 
```
Here is a screenshot from VS Code:
![Image](Lab3_VSCode.png)

**Step 2**
Now, when I go to terminal, I would only need to type in `ieng6` to log into ieng6 instead of the entire email address. This would help save a lot of time. 

Here is a screenshot from logging in:

**Step 3**
In addition, I would now be able to move around files using `scp` with just typing in `ieng6`. Here is what that looks like:


## Task 2: Setup Github Access from ieng6
