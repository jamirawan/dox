---
layout: default
title: Lists
parent: Markdown
nav_order: 6
has_children: false
has_toc: false

---


# Lists
## Unordered

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

## Ordered

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

## Elements in Lists

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
1.  This list will include image
2.  This is Irawan's logo
    ![Irawan](https://irawan.io/og/irawan-io.png)
3.  So that's a logo
```

***Rendered output***

1.  This list will include image
2.  This is Irawan's logo
    ![Irawan](https://irawan.io/og/irawan-io.png)
3.  So that's a logo

