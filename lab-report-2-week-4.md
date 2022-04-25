# CSE 15L Lab 2 

> __Name__ : Charvi Shukla 

> __Email__ : cshukla@ucsd.edu 

## Introduction

Hello! Welcome to my Lab report #2 for CSE 15L! For the purpose of this lab report, I will be utilizing the MarkdownParse experiment we did in the Lab section for weeks 3 and 4. I worked on the `markdown-parse` lab experiment with George during class time, and forked his repository.

## Screenshot for code change

Here is what our code change page looks like:

![Image](changes_screenshot1.png)

![Image](changes_screenshot2.png)

Click [here](https://github.com/charvishukla/markdown-parser/commit/2880d403612786f485cc0db46e56594b8c0de3d1) to see the page.

## Link to the test file for a _failure-inducing input

A **failiure-inducing input** is an input to the program that allows buggy code to execute, leading to symptoms. Symptoms are essentially wrong outputs or situations where the code crashes. 

This [testfile](https://github.com/charvishukla/markdown-parser/blob/main/fail1.md) is an example of a failiure inducing input. The file, called `fail1.md` does not have any contents. This causes errors while running with the original version of `MarkdownParse.java`.

In order to fix this problem we added the following lines of code to the file:

```
if(markdown.length() == 0){
    return(null);
}
```

This change can be seen in lines 14, 15, and 16 in the code change screenshot above. 

## The symptom of that _failure-inducing input_

The failure-inducing input here is the testfile called [fail1.md](https://github.com/charvishukla/markdown-parser/blob/main/fail1.md). It causes a `StringIndexOutOfBoundsException` which looks as following in the terminal:

![Image](errormessage.png)

A `StringIndexOutOfBoundsException` happens when the code tries to access either a negative or an index bigger than the length of the string. 

## The **bug**, the **symptom**, and the **failiure-inducing input**

The bug in this scenario is the missing code that account for empty files. When a _failiure-inducing input_, i.e. an empty .md file is used, the symptom is seen. Here, the symptom is a `StringIndexOutOfBoundsException` being thrown. 

## Correct Code Output 


## Conclusion 
This conculdes my lab report #2. Thank you for reading! 


Sources Used: [How To Debug](https://blog.regehr.org/archives/199)

