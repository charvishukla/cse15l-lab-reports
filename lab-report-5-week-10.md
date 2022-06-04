# CSE 15L Lab 4

> __Name__ : Charvi Shukla 

> __Email__ : cshukla@ucsd.edu 

## INTRODUCTION
Welcome to my lab report 5 for CSE 15L!


## TASK 1

**I. Finding the differing results**

To find the different results, I did the following steps:

1. Step 1: Copied the directory containing all the test files over, from the given repository, to my own repository. To do that, I used the following command:

`cp -r cse15lsp22-markdown-parser/test-files markdown_parser_2/`

2. Step 2: Copied the `script.sh` file using the command: 

`cp cse15lsp22-markdown-parser/script.sh markdown_parser_2/`

3. Step 3: Then, I copied over all the results of running those test files into `results.txt`. To do that, I used the command:

`bash script.sh > results.txt`

4. Step 4: Repeat the same thing for the cloned repository. [Given repository](https://github.com/nidhidhamnani/markdown-parser)

5. Step 5: Used `vimdiff` to compare the differences. I used the following command to do so:

`vimdiff markdown_parser_2/results.txt cse15lsp22-markdown-parser/results.txt`

![Image](res_compare%20.png)

**The results on the right are the results from runnning the tests with the given repository, while the ones on the right are the ones that were ran on my version on markdown parser**

## TASK 2 
**DIFFERING TEST FILES I CHOSE**

> `test-files/41.md`

Contents:
![Image](test41contents.png)

Test result: 
![Image](test41.png)

[Commit Link for 41](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/41.md)


> `test-files/495.md`

Contents

![Image](test498contents.png)

Test result:
![Image](test495.png)

[Commit Link for 495](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/495.md)

## TASK 3 

**Figuring out the correct expected output**

To get the correct expected output for parsing the contents of these given files, I will be using the [common mark website](https://spec.commonmark.org/dingus/)

Expected output for `41.md`
![Image](41_expected.png)

Expected output for `495.md`
![Image](495_expected.png)

**Test file 41**

From analysing this we can see that the result for `41.md` should simply be `[]` since common mark does not recognize any of the inputs as Links.

We can see that the given code produces the correct output, i.e. it results in empty brackets. On the other hand, simply returns a message indicating to the user that the input is incorrect. 

![Image](test41.png)

**Test file 495**

From analysing the output result in common mark, we can see that the expected output should be the embedded "link" `foo(and(bar))`
The output from the given repository does produce the correct output.

However, my output has 2 problems: (1) it prints out an error message for no reason. (2) it misses a parenthesis in the second line of the output. 

Instead of printing `foo(and(bar))`, my output prints `foo(and(bar)`

![Image](test495.png)


## POETENTIAL CHANGES 

**Test file 41**

![Image](CHANGE1.png)

Instead of throwing the error messages in lines 30 and 31, I could just return `"[]"` instead. This would make my ouput match the output required by common mark. 

**Test file 495**

![Image](CHANGE2.png)

The current expected input contains a set of nested parentheses. To fix this, another feild called `openParenthesisCounter` and `closeParenthesisCounter`could be added to line 19 and 20. This can then be used to keep track of all the possible parentheses in a link, and ensure that the current markdown parser reads the substrings between approprate indices.

![Image](CHANGE1.png)

In addition, a condition can be added to all of these if statements so that the statement does not execute immediately if there are multiple parentheses and accounts for the entire string before going in the if statement. 


## CONCLUSION

This concludes my 5th lab report! Thank you for reading! :) 