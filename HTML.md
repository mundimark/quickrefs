# HTML <=>  Markdown Quick Reference


HTML                            | Notes
------------------------------- | ---------------------
`<h1>...</h1>` - `<h6>...</h6>` | Heading 1-6
`<p>...</p>`                    | Paragraph
`<br>`                          | Hard Line Break 
`<i>...</i>`                    | Italic Text (Emphasis)
`<b>...</b>`                    | Bold Text (Strong Emphasis)
`<code>...</code>`              | Code (Monospace Text)
`<del>...</del>`                | Deleted (Strikethrough) Text
`<ul>(<li>...</li>)+</ul>`      | Unordered List
`<ol>(<li>...</li>)+</ol>`      | Ordered (Numbered) List
`<a href="...">...</a>`         | Link
`<img src="..." alt="...">`                   | Image (with Alternative Text)
`<table>(<tr>(<td>...</td>)+</tr>)+</table>`  | Table
`<pre><code>...</code></pre>`                 | Preformatted Code Block
`<blockquote>...<blockquote>`                 | Blockquote
`<hr>`                          | Horizontal Rule
`<!-- ... -->`                  | Comments  



## `<h1>...</h1>` - `<h6>...</h6>` - Heading 1-6

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

  or

```
Heading 1
=========

Heading 2
---------
```


## `<p>...</p>` - Paragraph

```
This is a paragraph. Paragraphs are separated
by a blank line.

This is another paragraph.
```

## `<br>` -  Hard Line Break 

```
Leave two spaces at the end of a line to do a line break.··↵
This is a new line.··↵
This is another new line.
```

## Text Formatting

_Italic • Bold • Code (Monospaced) • Deleted (Strikethrough)_

### `<i>...</i>` - Italic Text (Emphasis)

```
This text is *italic*.
```

or

```
This text is _italic_ too.
```

### `<b>...</b>` - Bold Text (Strong Emphasis)

```
This text is **bold**. 
```

or

```
This text is __bold__ too.
```

### `<code>...</code>` -  Code (Monospace Text)

```
This text is `monospaced`.
```

### `<del>...</del>` - Deleted (Strikethrough) Text

```
This text is ~~deleted~~.
```



## Lists

_Unordered • Ordered (Numbered)_ 

### `<ul>(<li>...</li>)+</ul>` - Unordered List

```
- Item 1
- Item 2
  - Item 2a        -- indent nested list with two spaces or more
  - Item 2b
```

 or

```
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

or

```
+ Item 1
+ Item 2
  + Item 2a
  + Item 2b
```

### `<ol>(<li>...</li>)+</ol>` - Ordered (Numbered) List

```
1. A list item
2. Another list item
   - A sublist item
   - Another sublist item
```



## `<a href="...">...</a>`  - Link

_Inline • Reference • Automatic_


### Inline

```
[Link Text](http://example.com)
[Link Text](http://example.com "Title")     -- add title attribute
[Link Text](/quickrefs/readme.html)         -- use absolute path (starts with /)
[Link Text](../readme.html)                 -- use relative path
[Link Text](#chapter1)                      -- use intra-page anchors

```

### Reference

```
[Link Text][id]
[GitHub][github]
[Git][git]
[Mastering Markdown][1]
[Markdown Basics][2]

...

[id]:     http://example.com
[github]: http://github.com                                -- use alphanumberic ids
[git]:    http://git-scm.com  "Offical Git Site"           -- add title attribute
[1]:      http://guides.github.com/mastering-markdown      -- use numeric ids
[2]:      http://help.github.com/articles/markdown-basics"
```


<!-- todo/check:
     also works with []() ??? -->



### Automatic

```
<http://example.com>
<http://github.com>
<http://guides.github.com/mastering-markdown>
```



## `<img src="..." alt="...">` - Image (with Alternative Text)

_Inline • Reference_

### Inline

```
![Alt Text](http://example.com/logo.png)
![Text](/i/logo.png)                     -- use absolute path (starts with \)
![Text](../logo.png)                     -- use relative path
![](logo.png)                            -- alternative text optional e.g. leave empty
![](logo.png "Title")                    -- add title attribute
```

### Reference

```
![Alt Text][logo]
![Text][1]
![Text][2]
![][3]

...

[logo]: http://example.com/logo.png
[1]:    /i/logo.png                     -- use absolute path (starts with \)
[2]:    ../logo.png                     -- use relative path
[3]:   logo.png  "Title"                -- add title attribute
```




## `<table>(<tr>(<td>...</td>)+</tr>)+</table>` - Table

_Standard • Options_ 

### Standard

```
| Header A | Header B | Header C |
| -------- | -------- | -------- |
| Text A1  | Text B1  | Text C1  |
| Text A2  | Text B2  | Text C2  |
```

or

```
Header A | Header B | Header C
-------- | -------- | --------
Text A1  | Text B1  | Text C1
Text A2  | Text B2  | Text C2
```

### Options


```
| Left     | Centered  |    Right |     
| -------- | :-------: | -------: |     --  use :---- for left aligned
| Text     |    Yes    |     12.3 |     --  use :---: for centered
| Text     |    Yes    |    567.8 |     --  use ----: for right aligned

```



## `<pre><code>...</code></pre>`  - Preformatted Code Block


```
This is comma-separated values (CSV) example:

····Date,Team1,Team2,FT,HT                      -- indent with four spaces
····2013-08-17,Arsenal,Aston Villa,1-3,1-1
····2013-08-17,Liverpool,Stoke,1-0,1-0
····2013-08-17,Swansea,Man United,1-4,0-2
····2013-08-18,Chelsea,Hull,2-0,2-0
```

or


    This is comma-separated values (CSV) example:
    
    ```                                     -- wrap with three backticks (`)
    Date,Team1,Team2,FT,HT
    2013-08-17,Arsenal,Aston Villa,1-3,1-1
    2013-08-17,Liverpool,Stoke,1-0,1-0
    2013-08-17,Swansea,Man United,1-4,0-2
    2013-08-18,Chelsea,Hull,2-0,2-0
    ```



## `<blockquote>...<blockquote>`  -  Blockquote


```
As Grace Hopper said:

> I've always been more interested
> in the future than in the past.
```

or


```
As Grace Hopper said:

> I've always been more interested
in the future than in the past.           -- shortcut version (> only required for first line)
```


## `<hr>` - Horizontal Rule

```
---           -- three or more dashes
```

 or   

```
- - -
```

 or

```
***          -- three or more asterix
```

or

```
* * *
```

or

```
___          -- three or more underscores
```


## `<!-- ... -->` - Comments  

```
<!-- Add your comments here. -->
```

or

```
<!-- 
    Add your comments here. 
  -->
```

## Appendix

### Escapes

#### Markdown Escapes

Note: Use the backslash (`\`) to escape special markdown characters:

```
\\       => \ ackslash
\`       => ` backtick
         => * asterisk
         => _ underscore
\{ or \} => {} curly braces
\[ or \] => [] square brackets
\( or \) => [] parentheses
\#       => # hash mark
\+       => + plus sign
\-       => - minus sign (hyphen / dash)
\.       => . dot
\!       => ! exclamation mark
```


#### HTML Entities in Code & Code Blocks 

Note: HTML entities in code and code blocks get auto-escaped:

```
<     =>  &lt;
>     =>  &gt;
&     =>  &amp;
```

### Pretty Printing

#### Quotes & Dashes

```
"Hello, World"    =>
'Hello, World'    =>
--                =>
---               =>
```


#### Copyright & Trademarks

```
(c)  or (C)   => ©
(r)  or (R)   => ®
...
```


### Emojis

`:smile:` :smile: •
`:tata:`  :tata:  •
`:book:`  :book:  •
`:gem:`   :gem:   •
`:+1:`    :+1:   

and many more
