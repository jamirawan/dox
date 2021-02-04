# Basic Markdown Cheatsheet

## 1. Heading (example of Heading 2)

***Makdown***

```md
# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading
```

***Markdown***

### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


---
## 2. Paragraphs

*Notes:*
- To create paragraphs, use a blank line to separate one or more lines of text.
- Don't ident paragraphs with spaces or tabs

***Markdown***

```md
This is the first paragraph.

This is the second paragraph
```

***Rendered output:***

This is the first paragraph.

This is the second paragraph

---
## 3 Line Break

*Notes:*
- To create a line break, end a line with two or more spaces, and then type return
- *Or* use the `<br>` HTML tag

***Markdown***

```md
This is the first line. 
And this is the second line.
```

***On browser:***

This is the first line.  
And this is the second line.

***Alternative Makdown***

```md
First line with the HTML tag after.<br>
And the next line.
```

***Rendered output***

First line with the HTML tag after.<br>
And the next line.

---
## 4. Emphasis

***Makdown***

```md
**This is bold text**
__This is bold text__
*This is italic text*
_This is italic text_
We have **bold***italic*
This text is ***really important***
This text is ___really important___
This text is __*really important*__
This text is **_really important_**
```

***Rendered output***

**This is bold text**  
__This is bold text__  
*This is italic text*  
_This is italic text_  
We have **bold***italic*  
This text is ***really important***  
This text is ___really important___  
This text is __*really important*__  
This text is **_really important_**

---
## 5. Blockquotes

*Notes:*
- Space is needed after the marker `>`;
- You could just add only one `>` at the first line;
- Blockquotes can be nested
- Blockquotes can contain multiple paragraphs. Add a >  between the paragraphs.
- Blockquotes can contain other Markdown formatted elements. But not all elements can be used.

***Makdown***

```md
> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.
```

***Rendered output***

> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.

***Makdown***

```md
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

***Rendered output***

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

***Makdown***

```md
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

***Rendered output***

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.

---
## 6. Lists
### 6.1. Unordered

***Makdown***

```md

+ To start a list, there should be an empty line above
+ Create a list by starting a line with `+`, `-`, or `*`
- Changing the sign will add a linespace
+ Add text under an item  
This is a text under an item. Notice that there are two spaces at the end above.
- Sub-lists are made by indenting 2 spaces:
  * Item 2a
  * Item 2b
* Item 3

To end a list, there should be one empty line above.
```

***Rendered output***

+ To start a list, there should be an empty line above
+ Create a list by starting a line with `+`, `-`, or `*`
- Changing the sign will add a linespace
+ Add text under an item  
This is a text under an item. Notice that there are two spaces at the end above.
- Sub-lists are made by indenting 2 spaces:
  * Item 2a
  * Item 2b
* Item 3

To end a list, there should be one empty line above.

### 6.2. Ordered

***Makdown***

```md
1. Item 1
1. Item 2  
Notice that the sequence number is irrelevant. 
Markdown will change the sequence automatically when renderring. 
Notice that there are two spaces at the end above to make a new text under item.
3. Sub-lists are made by indenting 4 spaces
    1. Item 3a
    2. Item 3b
8. Any number for item 4
```

***Rendered output***

1. Item 1
1. Item 2  
Notice that the sequence number is irrelevant.  
Markdown will change the sequence automatically when renderring.  
Notice that there are two spaces at the end above to make a new text under item.
3. Sub-lists are made by indenting 4 spaces
    1. Item 3a
    2. Item 3b
8. Any number for item 4

***Makdown***

```md
57. will started with offset 57
1. so it will be 58
```

***Rendered output***

57. will started with offset 57
1. so it will be 58

---

## 7. Elements in Lists

*Notes:*
- To add another element in a list while preserving the continuity of the list, indent the element four spaces or one tab

***Makdown***

```md
* This is the first list item.
* Here's the second list item.
    I need to add another paragraph below the second list item.
* And here's the third list item.
```

***Rendered output***

* This is the first list item.
* Here's the second list item.
 I need to add another paragraph below the second list item.
* And here's the third list item.


***Rendered output***

*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.

***Rendered output***

*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.


***Makdown***

```md
1.  Open the file containing the Linux mascot.
2.  Linux mascot called Tux.
    ![Tux, the Linux mascot](https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Tux.png/220px-Tux.png)
3.  Tux is cool.
```

***Rendered output***

1.  Open the file containing the Linux mascot.
2.  Linux mascot called Tux.
    ![Tux, the Linux mascot](https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Tux.png/220px-Tux.png)
3.  Tux is cool.


*But, for text element in ordered list, add five spaces*

1.   This is the first list item.
2.   Here's the second list item.

     I need to add another paragraph below the second list item.

3.   And here's the third list item.

*But, for quote in ordered list, add five spaces*

1. This is the first list item.
3.   Here's the second list item.

     > A blockquote would look great below the second list item.

5.   And here's the third list item.

*But, for code blocks in the lists, add eight spaces or two tabs.*

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.


---
## 8. Code

*Notes:*
- Inline codes is written inside \` \`
- or idented by add four spaces or one tab before

***Makdown***

```md
This is inline `code`.
```

***Rendered output***

This is inline `code`.

For a block of codes add three backward single quotes

***Makdown***
````

``` javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
````

***Rendered output***

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 


***Makdown***

```md
    <html>
      <head>
        <title>Test</title>
      </head>
```

***Rendered output***

    <html>
      <head>
        <title>Test</title>
      </head>

---
## 9. Links

**Example**

This is [link](https://irawan.io))  
This is [link with title](https://irawan.io "Irawan's site")

*Or, directly put the link*

https://example.com/  
fake@example.com

*Or with `<>`*

<https://www.markdownguide.org>  
<fake@example.com>

*But, to prevent automated linking*

 `https://www.example.com`

*Or add emphasize*

This is the *[Markdown Guide](https://www.markdownguide.org)*.  
See the section on [`code`](#code).





*Or, put reference in text*

It was a [hobbit-hole][hh], and that means comfort.

[hh]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"

*But, be careful with spaces in the links, put `%20` as space*

[example %20 link](https://www.example.com/my%20great%20page)  
[example without %20](https://www.example.com/my great page)

---
## 11. Images

*Notes:*
- It is not recommended to use image links in reference format. Some apps will not preview those images.
- Specifying size of image is supported only in some extended markdown (such as *markdown-it*).

***Makdown***

```md
![Irawan's Image](https://irawan.io/og/irawan-io.png
![Image Alt Text](https://irawan.io/og/irawan-io.png "Irawan's logo")
![Image Alt Text](https://irawan.io/og/irawan-io.png "Image specified with width and height" =800x600)
![Image Alt Text](https://irawan.io/og/irawan-io.png=800x600)
![Image Alt Text](https://irawan.io/og/irawan-io.png"Image specified with width" =800x)
![Image Alt Text](https://irawan.io/og/irawan-io.png"Image specified with height" =x600)
```

***Rendered output***

![Irawan's Image](https://irawan.io/og/irawan-io.png)
![Image Alt Text](https://irawan.io/og/irawan-io.png "Irawan's logo")
![Image Alt Text](https://irawan.io/og/irawan-io.png "Image specified with width and height" =800x600)
![Image Alt Text](https://irawan.io/og/irawan-io.png=800x600)
![Image Alt Text](https://irawan.io/og/irawan-io.png"Image specified with width" =800x)
![Image Alt Text](https://irawan.io/og/irawan-io.png"Image specified with height" =x600)


## 12. Emphasis 

### Bold
Two asterisks around the words will make it bold

***Markdown***
```md
This **word** is bold. 

```
***Rendered output***

This **word** is bold. 

### Italic

One asterisk will make it italic

```md
This *word* is italic
```

***Rendered output***
This *word* is italic

## 12 Horizontal lines

***Markdown***
```md
___

---

***

```

***Rendered output***

___
---
***
```
