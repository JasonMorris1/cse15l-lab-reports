
The following file caused an 
infinite loop to occur in the program.

[File1](https://github.com/JasonMorris1/markdown-parser/blob/main/nolink.md)

```
Exception in thread "main" java.lang.OutOfMemoryError: Java heap spac…
…e at java.base/java.util.Arrays.copyOf(Arrays.java:3512) at java.base/java.util.Arrays.copyOf(Arrays.java:3481) at java.base/java.util.ArrayList.grow(ArrayList.java:237) at java.base/java.util.ArrayList.grow(ArrayList.java:244) at java.base/java.util.ArrayList.add(ArrayList.java:454) at java.base/java.util.ArrayList.add(ArrayList.java:467) at MarkdownParse.getLinks(MarkdownParse.java:19) at MarkdownParse.main(MarkdownParse.java:30)

```

The code was fixed in this commit

![Error1](/assets/images/error1.png)
