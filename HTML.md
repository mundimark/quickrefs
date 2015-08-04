# HTML <=>  Markdown Reference


HTML                            | Notes                
------------------------------- | --------------------- 
`<h1>...</h1>` - `<h6>...</h6>` | Heading 1-6
`<p>...</p>`                    | Paragraph
`<br>`                          | Hard Line Break 
`<i>...</i>`                    | Italic Text (Emphasis)
`<b>...</b>`                    | Bold Text (Strong Emphasis)
`<code>...</code>`              | Code (Monospace Text)
`<del>...</del>`                | Deleted (Strike-through) Text
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
Leave two spaces at the end of a line to do a line break.••↵
This is a new line.••↵
This is another new line.
```

## Text Formatting

Italic • Bold • Code (Monospaced) • Deleted (Strike-Through)

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

### `<del>...</del>` - Deleted (Strike-through) Text 

```
This text is ~~deleted~~.
```


## Lists

Unordered • Ordered (Numbered)

### `<ul>(<li>...</li>)+</ul>` - Unordered List

```
- Item 1
- Item 2
- Item 3
```

 or

```
* Item 1
* Item 2
* item 3
```

or

```
+ Item 1
+ Item 2
+ Item 3
```

### `<ol>(<li>...</li>)+</ol>` - Ordered (Numbered) List

```
1. A list item
2. Another list item
3. Yet another list item
```


## `<hr>` - Horizontal Rule

```
---       
```

 or   

```
- - -
```

 or

```
***
```

or

```
* * *
```


## `<img src="..." alt="...">` - Image (with Alternative Text)

```
![Text](http://example.com/logo.png)
![Text](logo.png)                       -- use relative path
![](logo.png)                           -- alternative text optional e.g. leave empty
```

## `<!-- ... -->` - Comments  

```
<!--
   Add your comments here.
  -->
```



add more html referecenes 
