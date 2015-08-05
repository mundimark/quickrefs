# HTML <=>  Markdown Quick Reference


HTML                            | Notes
------------------------------- | ---------------------
`<h1>...</h1>` - `<h6>...</h6>`             | Header 1-6
`<p>...</p>`                                | Paragraph
`<br>`                                      | Hard Line Break 
`<i>...</i>` or `<em>...</em>`              | Italic Text (Emphasis)
`<b>...</b>` or `<strong>...</strong>`      | Bold Text (Strong Emphasis)
`<code>...</code>`              | Code (Monospace Text)
`<del>...</del>`                | Deleted (Strikethrough) Text
`<ul>(<li>...</li>)+</ul>`      | Unordered (Bullet) List
`<ol>(<li>...</li>)+</ol>`      | Ordered (Numbered) List
`<a href="...">...</a>`         | Link
`<img src="..." alt="...">`                   | Image with Alt(ernative) Text
`<table>(<tr>(<td>...</td>)+</tr>)+</table>`  | Table
`<pre><code>...</code></pre>`                 | Preformatted Code Block
`<blockquote>...<blockquote>`                 | Blockquote
`<hr>`                          | Horizontal Rule
`<!-- ... -->`                  | Comments




## Header 1-6 - `<h1>...</h1>` - `<h6>...</h6>`

```
# Header 1
## Header 2
### Header 3
#### Header 4 ####
##### Header 5 #####
###### Header 6 ######
```

Resulting in:

# Header 1
## Header 2
### Header 3
#### Header 4 ####
##### Header 5 #####
###### Header 6 ######

</>

  or

```
Header 1
=========

Header 2
---------
```

Resulting in:

Header 1
=========

Header 2
---------

</>



## Paragraph - `<p>...</p>`

```
This is a paragraph. Paragraphs are separated
by a blank line.

This is another paragraph.
```

Resulting in:

This is a paragraph. Paragraphs are separated
by a blank line.

This is another paragraph.

</>


## Hard Line Break - `<br>`

```
Leave two spaces at the end of a line to do a line break.··↵
This is a new line.··↵
This is another new line.
```

Resulting in:

Leave two spaces at the end of a line to do a line break.  
This is a new line.  
This is another new line.

</>



## Text Formatting

_Italic (Emphasis) • Bold (Strong Emphasis) • Code (Monospaced) • Deleted (Strikethrough)_

### Italic Text (Emphasis) - `<i>...</i>` or `<em>...</em>`

```
This text is *italic*.
```

or

```
This text is _italic_ too.
```

Resulting in:

This text is *italic*.  
This text is _italic_ too.

</>



### Bold Text (Strong Emphasis) - `<b>...</b>` or `<strong>...</strong>`

```
This text is **bold**. 
```

or

```
This text is __bold__ too.
```

Resulting in:

This text is **bold**.  
This text is __bold__ too.

</>


### Code (Monospace Text) - `<code>...</code>`

```
This text is `monospaced`.
```

Resulting in:

This text is `monospaced`.

</>


### Deleted (Strikethrough) Text - `<del>...</del>`

```
This text is ~~deleted~~.
```

Resulting in:

This text is ~~deleted~~.

</>



## Lists

_Unordered (Bullet) • Ordered (Numbered)_ 

### Unordered (Bullet) List - `<ul>(<li>...</li>)+</ul>`

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

Resulting in:

- Item 1
- Item 2
  - Item 2a
  - Item 2b

</>


### Ordered (Numbered) List - `<ol>(<li>...</li>)+</ol>`

```
1. A list item
2. Another list item
   - A sublist item
   - Another sublist item
```

Resulting in:

1. A list item
2. Another list item
   - A sublist item
   - Another sublist item

</>


## Link - `<a href="...">...</a>`


_Inline • Reference • Automatic_


### Inline

```
[Link Text](http://example.com)
[Link Text](http://example.com "Title")     -- add title attribute
[Link Text](/quickrefs/readme.html)         -- use absolute path (starts with /)
[Link Text](../readme.html)                 -- use relative path
[Link Text](#chapter1)                      -- use intra-page anchors

```

<!-- note: use example.com for all "live" links
  -->

Resulting:

[Link Text](http://example.com)
[Link Text](http://example.com "Title")
[Link Text](http://example.com/quickrefs/readme.html)
[Link Text](http://example.com/test/../readme.html)
[Link Text](http://example.com/#chapter1)

</>


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
[2]:      http://help.github.com/articles/markdown-basics
```

<!-- todo/check:
     also works with []() ??? -->


Resulting in:

[Link Text][id]
[GitHub][github]
[Git][git]
[Mastering Markdown][1]
[Markdown Basics][2]

[id]:     http://example.com
[github]: http://github.com
[git]:    http://git-scm.com  "Offical Git Site"
[1]:      http://guides.github.com/features/mastering-markdown
[2]:      http://help.github.com/articles/markdown-basics

</>



### Automatic

```
<http://example.com>
<http://github.com>
<http://help.github.com/articles/markdown-basics>
```

Resulting in:

<http://example.com>
<http://github.com>
<http://help.github.com/articles/markdown-basics>

</>



## Image with Alt(ernative) Text - `<img src="..." alt="...">`

_Inline • Reference_

### Inline

```
![Alt Text](http://example.com/logo.png)
![Text](/i/logo.png)                      -- use absolute path (starts with \)
![Text](../logo.png)                      -- use relative path
![](logo.png)                             -- alternative text optional e.g. leave empty
![](logo.png "Title")                     -- add title attribute
```


<!-- to be done
     add logo example to repo??
  -->

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

Resulting in:

| Header A | Header B | Header C |
| -------- | -------- | -------- |
| Text A1  | Text B1  | Text C1  |
| Text A2  | Text B2  | Text C2  |

</>

### Options


```
| Left     | Centered  |    Right |     
| -------- | :-------: | -------: |     --  use :---- for left aligned
| Text     |    Yes    |     12.3 |     --  use :---: for centered
| Text     |    Yes    |    567.8 |     --  use ----: for right aligned

```

Resulting in:

| Left     | Centered  |    Right |
| -------- | :-------: | -------: |
| Text     |    Yes    |     12.3 |
| Text     |    Yes    |    567.8 |

</>


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

Resulting in:

This is comma-separated values (CSV) example:

    Date,Team1,Team2,FT,HT
    2013-08-17,Arsenal,Aston Villa,1-3,1-1
    2013-08-17,Liverpool,Stoke,1-0,1-0
    2013-08-17,Swansea,Man United,1-4,0-2
    2013-08-18,Chelsea,Hull,2-0,2-0

</>


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
in the future than in the past.     -- shortcut version; email-style quote (>) only required in first line
```

Resulting in:

As Grace Hopper said:

> I've always been more interested
> in the future than in the past.

</>


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

Resulting in:

---

</>


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

Resulting in:

</>


## Appendix

### Escapes

#### Markdown Escapes

Note: Use the backslash (`\`) to escape special markdown characters:

```
\\        =>  \ ackslash
\`        =>  ` backtick
\*        =>  * asterisk          e.g. \*literal asterisks\*     -- no bold text
\_        =>  _ underscore
\{ or \}  =>  {} curly braces
\[ or \]  =>  [] square brackets
\( or \)  =>  [] parentheses
\#        =>  # hash mark 
\+        =>  + plus sign
\-        =>  - minus sign (hyphen / dash)
\.        =>  . dot               e.g. 2020\. What a great year.  -- no numbered list item
\!        =>  ! exclamation mark
```


#### HTML Entities in Code & Code Blocks 

Note: HTML entities in code and code blocks get auto-escaped:

```
<    =>  &lt;
>    =>  &gt;      e.g. <html> => &lt;html&gt;
&    =>  &amp;
```


### Pretty Printing

#### Quotes, Dashes, and Ellipses

Text              | Pretty            | Notes
----------------- | ----------------- | -------------------------------------
`"Hello, World"`  |  “Hello, World”   | uses “ (`&ldquo;`) and ” (`&rdquo;`)
`'Hello, World'`  |  ‘Hello, World’   | uses ‘ (`&lquo;`) and ’ (`&rquo;`) 
`--`              |  –                | uses –  (`&ndash;`)
`---`             |  —                | uses — (`&mdash;`)
`...`             |  …                | uses … (`&hellip;`)

...



#### Copyright & Registered Trademark

Text           | Pretty     | Notes
-------------- | ---------- | -------------------
`(c)` or `(C)` |  ©         | uses © (`&copy;`)
`(r)` or `(R)` |  ®         | uses ® (`&reg;`)

...


### Emoji (Shortcodes)

Text             | Emoji
---------------- | -----
`:smile:`        | :smile:
`:wink:`         | :wink:
`:grin:`         | :grin:
`:sunglasses:`   | :sunglasses:
`:rage:`         | :rage:
`:tada:`         | :tada: 
`:book:`         | :book: 
`:gem:`          | :gem:  
`:+1:`           | :+1:   

and many more


## Meta

**Thanks**

Michel Fortin • Waylan Limberg  

**License**

The quick reference is dedicated to the public domain. Use it as you please with no restrictions whatsoever.

**Questions? Comments?**

Send them along to the markdown-discuss mailing list. Thanks!



