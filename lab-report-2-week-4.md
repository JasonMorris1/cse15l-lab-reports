
The following file caused an 
infinite loop to occur in the program.

[Test File 1](https://github.com/JasonMorris1/markdown-parser/blob/main/nolink.md)

```
Exception in thread "main" java.lang.OutOfMemoryError: Java heap spac…
…e at java.base/java.util.Arrays.copyOf(Arrays.java:3512) at java.base/java.util.Arrays.copyOf(Arrays.java:3481) at java.base/java.util.ArrayList.grow(ArrayList.java:237) at java.base/java.util.ArrayList.grow(ArrayList.java:244) at java.base/java.util.ArrayList.add(ArrayList.java:454) at java.base/java.util.ArrayList.add(ArrayList.java:467) at MarkdownParse.getLinks(MarkdownParse.java:19) at MarkdownParse.main(MarkdownParse.java:30)

```

The out of memory symptom was fixed by finding the bug and fixing it. A break was added in the code when `markdown.indexOf("[", currentIndex);` returns -1. When we can not find the first starting character of a new link we break out of the while loop as there are no more links. 

![Error1](/assets/images/error1.png)


***
[Test file 2](https://github.com/JasonMorris1/markdown-parser/blob/066335a1ae1b43d45ec9de511ec5d90beac9dac9/test2.md)

This test file was producing the same out of memory error. We fixed it by providing break statements for the rest of the function calls to `markdown.indexOf(...)` so if we can't find the expected parenthesis or brackets there can not possibly be anymore links in the remaining String so we break.

![Error2](/assets/images/error2.png)

