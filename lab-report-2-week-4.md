[Home](https://jasonmorris1.github.io/cse15l-lab-reports/)
[google](www.google.com)
# Code Change 1
The following file caused an 
infinite loop to occur in the program which is a symptom of a bug in our code.

[Test File 1](https://github.com/JasonMorris1/markdown-parser/blob/main/nolink.md)

```
Exception in thread "main" java.lang.OutOfMemoryError: Java heap spac…
…e at java.base/java.util.Arrays.copyOf(Arrays.java:3512) at java.base/java.util.Arrays.copyOf(Arrays.java:3481) at java.base/java.util.ArrayList.grow(ArrayList.java:237) at java.base/java.util.ArrayList.grow(ArrayList.java:244) at java.base/java.util.ArrayList.add(ArrayList.java:454) at java.base/java.util.ArrayList.add(ArrayList.java:467) at MarkdownParse.getLinks(MarkdownParse.java:19) at MarkdownParse.main(MarkdownParse.java:30)

```

The out of memory symptom was fixed by finding the bug and fixing it. A break was added in the code when `markdown.indexOf("[", currentIndex);` returns -1. When we can not find the first starting character of a new link we break out of the while loop as there are no more links. 

![Error1](/assets/images/error1.png)


---
# Code change 2

[Test file 2](https://github.com/JasonMorris1/markdown-parser/blob/066335a1ae1b43d45ec9de511ec5d90beac9dac9/test2.md)

```
Exception in thread "main" java.lang.OutOfMemoryError: Java heap spac…
…e at java.base/java.util.Arrays.copyOf(Arrays.java:3512) at java.base/java.util.Arrays.copyOf(Arrays.java:3481) at java.base/java.util.ArrayList.grow(ArrayList.java:237) at java.base/java.util.ArrayList.grow(ArrayList.java:244) at java.base/java.util.ArrayList.add(ArrayList.java:454) at java.base/java.util.ArrayList.add(ArrayList.java:467) at MarkdownParse.getLinks(MarkdownParse.java:19) at MarkdownParse.main(MarkdownParse.java:30)

```

This test file was producing the same `Java heap space` error. We fixed it by providing break statements for the rest of the function calls to `markdown.indexOf(...)` so if we can't find the expected parenthesis or brackets there can not possibly be anymore links in the remaining String so we break.

![Error2](/assets/images/error2.png)

---
# Code change 3
```
…failure: 1) testforValidLink(MarkdownParseTest) java.lang.AssertionError: no valid links in file expected:<true> but was:<false> at org.junit.Assert.fail(Assert.java:89) at org.junit.Assert.failNotEquals(Assert.java:835) at org.junit.Assert.assertEquals(Assert.java:120) at MarkdownParseTest.testforValidLink(MarkdownParseTest.java:190) FAILURES!!! Tests run: 14, Failures: 1



```

The last bug we encountered was that a markdown image was being picked up as a link and returned in our parser method. 
[Test file 3](https://github.com/JasonMorris1/markdown-parser/blob/main/test-file6.md)

We fixed this bug by looking if there is an exclamation mark before and breaking if there is one. 
![image3](/assets/images/fix3.png)
This fix however introduced another bug in the code. The symptom was that when there was a image then a link in file the code failed to find the link. This was fixed by instead of breaking when an exclamation mark is found instead we look for the next open bracket essentially skipping the image and looking for the next link.

![image4](/assets/images/fix4.png)

---