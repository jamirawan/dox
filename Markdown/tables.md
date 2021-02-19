---
layout: default
title: Tables
parent: Markdown
nav_order: 9
has_children: false
has_toc: false

---

# Table styles on Markdown

## Headers
**Markdown**
```md
| Header Column One | Header Column Two | Header Column Three | Header Column Four |
```


## Alignments

Left align: `:--` or three dashes `---`
Right align: `--:`
Centre align: `:-:` 

Place those alignment within pipes in the respective columns.

**Markdown**

```md
| Default Header | Left Align | Right Align | Center Align |
| --- | :-- | --: | :-: |
```

## Table contents

Every columns is separated with pipe `|` and every row is placed in different lines:


**Markdown**

```md
| Column 1 Header | Column 2 Header | Column 3 Header |
| --------------- | --------------- | --------------- |
| Row 1 Column 1 | Row 1 Column 2 | Row 1 Column 3 |
| Row 2 Column 1 | Row 2 Column 2 | Row 2 Column 3 |
| Row 3 Column 1 | Row 3 Column 2 | Row 3 Column 3 |
```

**Output**

| Column 1 Header | Column 2 Header | Column 3 Header |
| --------------- | --------------- | --------------- |
| Row 1 Column 1 | Row 1 Column 2 | Row 1 Column 3 |
| Row 2 Column 1 | Row 2 Column 2 | Row 2 Column 3 |
| Row 3 Column 1 | Row 3 Column 2 | Row 3 Column 3 |
