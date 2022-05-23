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

```
1) testSnippet1(MarkdownParseTest)
array lengths differed, expected.length=3 actual.length=0; arrays first differed at element [0]; expected:<`google.com> but was:<end of array>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:89)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:285)
        at org.junit.Assert.assertArrayEquals(Assert.java:300)
        at MarkdownParseTest.testSnippet1(MarkdownParseTest.java:217)
        ... 32 trimmed
Caused by: java.lang.AssertionError: expected:<`google.com> but was:<end of array>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:87)
        ... 38 more
```
