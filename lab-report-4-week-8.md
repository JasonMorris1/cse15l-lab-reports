[Home](https://jasonmorris1.github.io/cse15l-lab-reports/)


# Lab Report 4 Week 8

[My MarkdownParse repo](https://github.com/JasonMorris1/markdown-parser)

[MarkdownParse review repo](https://github.com/ANGUYEN625/markdown-parser)

## Snippet 1
```md
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

## Snippet 1 Rendered
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)

## Snippet 1 Test

``` java
    @Test
    public void testSnippet1() {
        try {

            ArrayList<String> links = MarkdownParse.getLinks(readFile("snippet1.md"));
            List expected = List.of("`google.com", "google.com", "ucsd.edu");
            assertArrayEquals(expected.toArray(), links.toArray());

        } catch (IOException e) {
            // e.printStackTrace();
        }
    }
```

## My implementation
```
3) testSnippet1(MarkdownParseTest)
arrays first differed at element [0]; expected:<[`google].com> but was:<[url].com>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
```

## Peers Implementation 

```
5) testSnippet1(MarkdownParseTest)
arrays first differed at element [0]; expected:<[`google].com> but was:<[url].com>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
```

## Snippet 1 Code Fix
The following markdown line: ``` `[a link`](url.com) ``` Is being picked up as a link when it shouldn't because its not being rendered as a link. To fix this would be difficult. I think maybe if you check if there are two ticks that enclose either "[" or "]" or "(" then that would not count as a valid link. For some reason back ticks on the ")" still render a link.
 ``` [code](ucsd.ed`u)` ``` is rendered as a valid link
 This would be diffcult to code because you would need to keep track of all previous ticks and whether or not they have a closing tick.


## Snippet 2
```md
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
## Snippet 2 Rendered
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)

## Snippet 2 Test 

``` java
@Test
    public void testSnippet2() {
        try {

            ArrayList<String> links = MarkdownParse.getLinks(readFile("snippet2.md"));

            List expected = List.of("a.com", "a.com(())", "example.com");

            assertArrayEquals(expected.toArray(), links.toArray());
        } catch (IOException e) {
            // e.printStackTrace();
        }
    }
```

## My Implementation

```
2) testSnippet2(MarkdownParseTest)
array lengths differed, expected.length=3 actual.length=0; arrays first differed at element [0]; expected:<a.com> but 
was:<end of array>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:89)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
```
## Peers Implementation
```
6) testSnippet2(MarkdownParseTest)
array lengths differed, expected.length=3 actual.length=1; arrays first differed at element [0]; expected:<a.com[]> but was:<a.com[((]>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
```

## Snippet 2 Code Fix
A fix for this code would be quite involved. You would need to create multiple stacks where you keep track of parentheses, brackets, and escaped brackets in order to determine if a link should be rendered or not. For instance an escaped bracket or escaped parenthesis wouldn't be added or used to remove an open bracket from the stack. You would also need to check that you don't have escaped brackets or parenthesis in the markdown link structure like ``` \[my link](link.com) ```


## Snippet 3
```md
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```
## Snippet 3 Rendered
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text



## Snippet 3 Test

``` java
    @Test
    public void testSnippet3() {
        try {

            List expected = List.of("https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule");
            ArrayList<String> links = MarkdownParse.getLinks(readFile("snippet3.md"));
            assertArrayEquals(expected.toArray(), links.toArray());

        } catch (IOException e) {
            // e.printStackTrace();
        }
    }
```


## My Implementation

```
3) testSnippet3(MarkdownParseTest)
array lengths differed, expected.length=1 actual.length=2; arrays first differed at element [0]; expected:<https://[sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]> but was:<https://[www.twitter.com]>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
```

## Peers Implementation

```
 testSnippet3(MarkdownParseTest)
array lengths differed, expected.length=1 actual.length=2; arrays first differed at element [0]; expected:<[https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]> but was:<[
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
]>
```

## Snippet 3 Code Fix
This would be easy to fix. If there is a line break anywhere inside of the brackets [] or  the parenthesis's () then the link is not valid. There might be some  issues however as on Unix a new line is "\n" and on windows a new line is "\r\n".
