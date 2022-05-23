[Home](https://jasonmorris1.github.io/cse15l-lab-reports/)


# Lab Report 4 Week 8

[My MarkdownParse repo](https://github.com/JasonMorris1/markdown-parser)

[Markdown parse review repo](https://github.com/ANGUYEN625/markdown-parser)

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
1) testSnippet1(MarkdownParseTest)
array lengths differed, expected.length=3 actual.length=0; arrays first differed at element [0]; expected:<`google.com> but was:<end of array>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:89)
```

## Peers Implementation 

```
5) testSnippet1(MarkdownParseTest)
arrays first differed at element [0]; expected:<[`google].com> but was:<[url].com>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
```

## Snippet 1 Code Fix


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

## My Imp

```
2) testSnippet2(MarkdownParseTest)
array lengths differed, expected.length=3 actual.length=0; arrays first differed at element [0]; expected:<a.com> but 
was:<end of array>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:89)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
```
## Peers Imp
```
6) testSnippet2(MarkdownParseTest)
array lengths differed, expected.length=3 actual.length=1; arrays first differed at element [0]; expected:<a.com[]> but was:<a.com[((]>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
```

## Snippet 2 Code Fix



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


## My Imp

```
3) testSnippet3(MarkdownParseTest)
array lengths differed, expected.length=1 actual.length=2; arrays first differed at element [0]; expected:<https://[sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]> but was:<https://[www.twitter.com]>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
```

## Peers Imp.

```
 testSnippet3(MarkdownParseTest)
array lengths differed, expected.length=1 actual.length=2; arrays first differed at element [0]; expected:<[https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]> but was:<[
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
]>
```

## Snippet 3 Code Fix