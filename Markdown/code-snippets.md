---
layout: default
title: Code snippets
parent: Markdown
nav_order: 6
has_children: false
has_toc: false

---


# Code snippets in markdown

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
````md

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
## Escaping markdown code block within markdown page
To escape block code as above or to display markdown code within markdown with three backticks included without being rendered, use either four backticks or three ~~~ 

***Makdown***

`````

````md

```md
> Nasi goreng is delicious...
>> ...if you like Asian food...
> > > ...good with spicy chilli sauce and cold beer.
```
````
# or
~~~md

```md
> Nasi goreng is delicious...
>> ...if you like Asian food...
> > > ...good with spicy chilli sauce and cold beer.
```
~~~

`````
***Rendered output***
````md

```md
> Nasi goreng is delicious...
>> ...if you like Asian food...
> > > ...good with spicy chilli sauce and cold beer.
```
````
to display above md snippet, add 5 backticks etc...
