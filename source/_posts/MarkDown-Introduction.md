---

title: MarkDown 介紹
categories: 
  - tech
tags: 
 - MarkDown
date: 2016-12-02 00:03:12
updated: 2017-11-05 16:18:20

---

Markdown 是一個輕量的標記語言，主要目的是讓人們可以不用 HTML 等複雜繁長的語法就能夠標記格式進而達到管理文件的目的。

### 標題（Header）###

Markdown支援兩種標題的語法，Setext 和 Atx 形式。
Setext 形式是用底線的形式，利用 `=`（最高階標題）和 `-`（第二階標題），例如：

```
This is an H1
=============

This is an H2
-------------
```

任何數量的 `=` 和 `-` 都可以有效果。

Atx 形式則是在行首插入 1 到 6 個 `#`，各對應到標題 1 到 6 階，在結尾加上任意 `#` (通常都會加上對等的數量)，例如：

```
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

<!-- more -->

---------------------------------------

### 段落（Paragraph）###

在 Markdown 中，只要是連續的行就會被當成 HTML 中的 paragraph。 在使用上，一般要將 paragraph 與 paragraph 之間以一個到數個空行間隔開來。  
若是只需要換行，則使用 `兩個 Space + Enter`，Markdown 會把這轉成一個 br 的標記。

---------------------------------------

### 水平分隔線（Horizontal Rules）###

三個或三個以上的符號，必須在獨立的一行，前後不能有其他文字。
短橫線（Hyphens）

```
---
```

半形星號（Asterisks）

```
***
```

下底線（Underscores）

```
___
```

---------------------------------------

### 引言（Block Quotes）###

Markdown 可以用 `>` 來標示文字區塊，就像在email裡一樣：

```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.
```

區塊引言可以有階層（例如：引言內的引言），只要根據層數加上不同數量的 `>`：

```
> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
```

引言的區塊內也可以使用其他的Markdown語法，包括標題、清單、程式碼區塊等：

```
> ## This is a header.
> 
> 1.   This is the first list item.
> 2.   This is the second list item.
> 
> Here's some example code:
> 
>     return shell_exec("echo $input | $markdown_script");
```

---------------------------------------

### 清單（Bullet Points）###

Markdown支援有序清單和無序清單。
無序清單使用星號、加號或是減號作為清單標記：

```
- Red
- Green
- Blue
```

有序清單則使用數字接著一個英文句點：

```
1. Bird
2. McHale
3. Parish
```

---------------------------------------

### 連結 ###

Markdown 支援兩種形式的連結語法：inline 和 reference 兩種形式。
行內：

```
This is [an example](http://example.com/ "Title") inline link.
[This link](http://example.net/) has no title attribute.
```

參考：

```
This is [an example][id] reference-style link.
[id]: http://example.com/  "Optional Title Here"
```

---------------------------------------

### 圖片 ###

Markdown 使用一種和連結很相似的語法來標記圖片，同樣也允許兩種樣式：inline 和 reference。
行內：

```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```

參考：

```
![Alt text][id]
[id]: url/to/image  "Optional title attribute"
```

---------------------------------------

### 粗體 ###

```
**Bold**
```

```
__Bold__
```

---------------------------------------

### 斜體 ###

```
*Italic*
```

```
_Italic_
```

---------------------------------------

### 刪除線 ###

```
~~Strike lines~~
```

---------------------------------------

### 表格 ###
冒號（Colons）是用來對齊的（擺左齊左、擺右齊右，都擺就置中）。
預設標題置中，內容置左。

| Text            | Align Center     | Align Right |  Align Left |
| --------------- |:----------------:| -----------:|:------------|
| content1        | Longer content1  |  content1   |   content1  |
| Longer content2 | content2         |  content2   |   content2  |
|         content3| content3         |  content3   |   content3  |


```
| Text            | Align Center     | Align Right |  Align Left |
| --------------- |:----------------:| -----------:|:------------|
| content1        | Longer content1  |  content1   |   content1  |
| Longer content2 | content2         |  content2   |   content2  |
|         content3| content3         |  content3   |   content3  |
```

---------------------------------------

### 程式碼 ###

如果要標記一小段行內程式碼，你可以用反引號（backticks）把它包起來（<code>`</code>），例如：

```
Use the `printf()` function.
```

若是要包起整段程式碼區塊可以用 <code>```</code> 把它包起來。


