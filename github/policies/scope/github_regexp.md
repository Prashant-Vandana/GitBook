---
description: >-
  Learn how to use regular expressions to exclude specific GitHub repositories,
  while configuring the scope section in Nightfall for GitHub.
---

# Use Regular Expressions to Exclude GitHub Directories

GitHub file paths do not contain the GitHub org name or repository names. They only contain the folder name(s) and file name. Hence a regular expression to match GitHub directories must only contain characters to just match the folder name and file name.&#x20;

## Matching Files at the Repository Level

These are the files that are directly located under a repository. They are not nested under any repository folders. If the file name is abcd.py and the repository name is Python repository, in a GitHub org called Python Project, then the file path would be Python Project/Python repository/abcd.py. However, as mentioned above, GitHub file paths do not include the GitHub org name and repository name, and hence the file path would just be abcd.py in this case.&#x20;

To exclude all such files (.py), you must create the regular expression as follows.

```regex
 .*\.py
```

Similarly, to exclude any other file types, you must replace `py` in the above pattern with your respective file extension.

## Matching Files Nested in Directories

You can match files nested under repositories, by using the escape sequence character (\\) for every level of nesting. An escape sequence character is required to match a forward slash (/) used in directories.

For instance, to match a file **abcd.py** under the folder **first** (effective GitHub file path is first/abcd.py), you must use the following regular expression.

```regex
first\/.*
```

The above expression matches all the files under the **first** folder and not just the **abcd.py**. To match only Python files (.py extension), you must use the following regular expression.

```regex
first\/.*\.py
```

To match only the **abcd.py** file, under the first folder, you must use the following regular expression.&#x20;

```regex
first\/abcd\.py
```

## Matching Nested Directories

To exclude all the files under a directory, you must match the entire directory. Consider that a directory is _first/second_. You wish to exclude all the files under this directory. Also, in this case, you must use the escape sequence character twice, since there are two levels of nesting and as a result, two forward slashes.&#x20;

```
first\/second\/.*
```

This regex matches and excludes all the files under the directory.

Similarly, to exclude files nested at multiple levels, you can use escape sequence character-based matching.&#x20;

## Cheat Sheet

This cheat sheet displays the regex to be used for various scenarios.

|                                       Match                                       |                                           Regex                                           |                                                             Comments                                                            |
| :-------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------: |
|                                   first/abcd.py                                   |     <pre class="language-regex"><code class="lang-regex">first\/abcd.py
</code></pre>     |                                 Match a file called abcd.py under a directory called **first**.                                 |
|               <p>first/abcd.py, first/efgh.py, <br>first/ijkq.py</p>              |      <pre class="language-regex"><code class="lang-regex">first\/.*.py
</code></pre>      |                              Match any file with .py extension under a directory called **first**.                              |
|            <p>first/abcd.py,<br>first/abcd.java,<br>first/abcd.cpp</p>            |        <pre class="language-regex"><code class="lang-regex">first\/.*
</code></pre>       |                                        Match any file under a directory called **first**.                                       |
|                                first/second/abcd.py                               | <pre class="language-regex"><code class="lang-regex">first\/second\/abcd.py
</code></pre> |    Match a file called abcd.py under a directory called **second,** which is nested under another direcory called **first**.    |
|   <p>first/second/abcd.py,<br>first/second/efgh.py, <br>first/second/ijkq.py</p>  |  <pre class="language-regex"><code class="lang-regex">first\/second\/.*.py
</code></pre>  | Match any file with .py extension under a directory called **second,** which is nested under another direcory called **first**. |
| <p>first/second/abcd.py,<br>first/second/efgh.java, <br>first/second/ijkq.cpp</p> |                             <pre><code>first\/.*
</code></pre>                            |           Match any file under a directory called **second,** which is nested under another direcory called **first**.          |
|                                      abcd.py                                      |         <pre class="language-regex"><code class="lang-regex"> .*.py
</code></pre>         |               Match a file called abcd.py which is located directly undet the repository and not under any folder.              |
|                     <p>abcd.py,<br>efgh.java, <br>ijkq.cpp</p>                    |           <pre class="language-regex"><code class="lang-regex">.*
</code></pre>           |                     Match any file which is located directly undet the repository and not under any folder.                     |



{% hint style="info" %}
You can use [this link](https://regex-generator.olafneumann.org/?sampleText=2020-03-12T13%3A34%3A56.123Z%20INFO%20%20%5Borg.example.Class%5D%3A%20This%20is%20a%20%23simple%20%23logline%20containing%20a%20%27value%27.\&flags=i) to generate a regular expression that exactly matches your requirements.
{% endhint %}
