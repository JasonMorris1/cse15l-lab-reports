[Home](https://jasonmorris1.github.io/cse15l-lab-reports/)

# Lab Report 5 

## Test  1 with different results
[Link to test file](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md)
Using vimdiff, I found that my implementation produced a different output for test file 201.md than the markdown implementation provided in lab 9. My implementation found no links where as the provided implementation found `baz` as a link in the file.
![img](/assets/images/vimdiff1.png)

Copying the contents of 201.md into Commommark.js website we can see what the correct output should be
![img](/assets/images/commonmark1.png)
As seen in the box on the right hand side the expected output has no links therefore my implementations was correct and the provided implementation has a bug. 