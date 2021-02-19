---
layout: default
title: Links
parent: Markdown
nav_order: 7
has_children: false
has_toc: false

---

# Links

To link text in markdown, just insert the linked tex in square bracket followed with round bracket of the URL, no space.

## Externarl links

**Markdown**
```md
This is [linked text](https://irawan.io) <br>
This is [link with title](https://irawan.io "Irawan's site")
```

**Rendered output**

This is [linked text](https://irawan.io)<br>
This is [link with title](https://irawan.io "Irawan's site")



### Directly put link on the address with `<>`

**Markdown**

```md
<https://www.irawan.io>  
<me@irawan.io>
```
**Output**

<https://www.irawan.io>  
<me@irawan.io>

## Internal link within Jekyll pages
There are many ways of doing this but here's the simplest I choose with `link` tags:

Markdown: `[Link text to Docker]({% link Docker/README.md %})`


**Output**

[Link text to Docker]({% link Docker/README.md %})

## Buttons
Button in MD is similar to links but add `{: .btn}` at the end

**Markdown**
```md
[Link button to my page](https://irawan.io){: .btn}
```
**Output**

[Link button to my page](https://irawan.io){: .btn}


## Prevent automated linking or skip linking
**Markdown**

```md
 `https://www.irawan.io`
 ```

**Output**

`https://www.irawan.io`

## Add emphasize/anchored link

**Markdown**

```md
This is the *[Irawan's site](https://www.irawan.io)*.  
See the section on [top of the page](#).
```
**Output**

This is the *[Irawan's site](https://www.irawan.io)*.  
See the section on [top of the page](#).




## Reference in text

**Markdown**

```md
It was a [nasi-goreng][ng], and that means comfort.

[ng]: <https://en.wikipedia.org/wiki/Nasi_goreng> "Nasi Goreng"
```
**Output**

It was a [nasi goreng][ng], a delicious Indonesian food.

[ng]: <https://en.wikipedia.org/wiki/Nasi_goreng> "Nasi Goreng"




