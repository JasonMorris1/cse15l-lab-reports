[Home](https://jasonmorris1.github.io/cse15l-lab-reports/)

# Lab Report 5 

## Test  1 with different results
[Link to test file](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md)
Using vimdiff, I found that my implementation produced a different output for test file 201.md than the markdown implementation provided in lab 9. My implementation found no links where as the provided implementation found `baz` as a link in the file.
![img](/assets/images/vimdiff1.png)

Copying the contents of 201.md into Commommark.js website we can see what the correct output should be:
![img](/assets/images/commonmark1.png)
As seen in the box on the right hand side the expected output has no links therefore my implementations was correct and the provided implementation has a bug. 

To fix the provided implementation we could add code that checks if the next character after the close bracket "]" is the open parenthesis character "(". To do this we could check if `openParen - nextCloseBracket = 1 ` and if this is not the case we don't consider this a valid link. By trying different input in Common Mark I found that any charters between [] and () cause the link to be invalid.

![img](/assets/images/codefix1.png)


## Test File 2
[TestFile Link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/22.md)



Test file 22 which contains 
``` 
[foo](/bar\* "ti\*tle")
``` 

produced a different result for my implementation which can be seen on the left side ov vimmdiff and the provided implementation on the right side.
![img](/assets/images/vimdiff2.png)

### Expected output
![img](/assets/images//commonmark2.png)
Since the expected output is a link my implementation provided the correct result, and the provided implementation output contained no links which is incorrect. 
If a link is provided where there is a space somewhere in the parenthesis () then the provided implementation considers this an invalid link. We can see that we only add the link to the list if the string containing the list returns -1 for the link string meaning there are no spaces inside the string. To fix this bug I would take this code out. 
![img](/assets/images/codefix2.png )

## Test File 3
[link to test file 496.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/496.md)
For this test file you can see the output of my implementation on the left and the provided implementation on the right.
![img](/assets/images/vimdiff3.png)
My implementation provides a link which is incorrect if you look at the rendered output of the contents of the testfile on common mark you can see that no links are rendered. The provided implementation produces the correct output.
![img](/assets/images/commonmark3.png)

### Code Fix
The bug in my code is that I am not checking for nested parenthesis. To fix this I would need to modify my getLinks method. The reason this markdown is not a link is because there are three opening parenthesis and only two closing parenthesis. The code I need to fix this bug would count the number of open parenthesis and the number of closed parenthesis and if there are more open parenthesis then the link would be considered invalid.

![img](/assets/images/codefix3.png)