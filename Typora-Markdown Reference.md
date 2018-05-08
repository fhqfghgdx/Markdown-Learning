[TOC]

# Block Elements

## Paragraph and line breaks

一个段落只是一个或多个连续的文本行。在Markdown源代码中，段落由多个空行分隔。在Typora中，您只需按回车即可创建一个新段落。

按下Shift + Enter 可创建一个换行符。但是，大多数markdown解析器会忽略单行换行，让其他markdown解析器识别您的换行符，您可以在行末留出两个空格，或者插入<br/>

## Headers

创建一级到六级标题

```markdown
# 标题1
## 标题2
...
###### 标题6
```

快捷键：

![标题快捷键](E:\OneDrive\GitHub\Markdown-Learning\Picture\标题快捷键.png)



## Blockquotes

使用 '>' 符号

```markdown
> This is a blockquote with two paragraphs. This is first paragraph.
```

> This is a blockquote with two paragraphs. This is first paragraph.
>
> This is second pragraph.Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> This is another blockquote with one paragraph. There is three empty line to seperate two blockquote.
>
> 在引用中再次引用
>
> > 二级引用第一段
> >
> > 二级引用第二段
> >
> > > 三级引用第一段
> > >
> > > ...

源码：

```markdown
> This is a blockquote with two paragraphs. This is first paragraph.
>
> This is second pragraph.Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> This is another blockquote with one paragraph. There is three empty line to seperate two blockquote.
>
> 在引用中再次引用
>
> > 二级引用第一段
> >
> > 二级引用第二段
> >
> > > 三级引用第一段
> > >
> > > ...
```



## Lists

无序列表：使用 '*'，'+'，'-'

有序列表：使用 '1.'，'2.'，...

### un-ordered list

+ Red
  + Green
    + Block
  + Yellow
    + Blue

源码：

```markdown
+ Red
  + Green
    + Block
  + Yellow
    + Blue
```

**注： 快捷键 Ctrl + / 切换视图为源代码模式**



### ordered list

1. Red
   1. Green
      1. Block
   2. Yellow
      1. Blue

源码：

```markdown
1. Red
   1. Green
      1. Block
   2. Yellow
      1. Blue
```



## Task list

创建任务列表形式的条目

- [x] A task list item
- [ ] list syntax required
  - [ ] normal **formatting** , @mentions, #1234 refs
  - [x] incomplete
  - [ ] complete

源码：

```markdown
- [x] A task list item
- [ ] list syntax required
  - [ ] normal **formatting** , @mentions, #1234 refs
  - [x] incomplete
  - [ ] complete
```



## (Fenced) Code Blocks

Typora 仅支持 GitHub 格式的代码块，而不支持 Markdown 原始代码块的格式。

使用 Fence 创建代码块：使用连续的三个 '```',Typora 将把其之后的行解析成代码块。

```markdown
Code block line 1
```

设置代码块语言：'```Python'

```python
import Serial
...
```



## Math Blocks

创建公式：两个连续的 '$$'

Input `$$`, then press ‘Return’ key will trigger an input field which accept *Tex/LaTex* source.  
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$

源码：

```markdown
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$
```



## Tables

Input `| First Header  | Second Header |` and press `return` key will create a table with two column. 

### 使用源码格式建立表格:

切换到Markdown源码视图输入下面的代码块

```markdown
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```

再切换回标准视图可以看到如下表格

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

### 使用 Typora 快速建立表格

**快捷键：Ctrl + T**，可以快速设置对齐方式，而不是使用 ':' 与 '-' 结合的方法

|      |      |      |
| ---- | ---- | ---- |
|      |      |      |
|      |      |      |
|      |      |      |



## Footnotes

You can create footnates like this[^1] and that[^2] .

[^1]: Here is the *this* of the **footnote**
[^2]: Here is the *that* of the **footnote**

源码：

```markdown
You can create footnates like this[^1] and that[^2] .

[^1]: Here is the *this* of the **footnote**
[^2]: Here is the *that* of the **footnote**
```



## Horizontal Rules

创建水平分割线：'***' 或 '---'

例如：

***

---

源码：

```
***

---
```



## YAML Front Matters

Typora support [YAML Front Matters](https://jekyllrb.com/docs/frontmatter/) now. Input `---` at the top of the article and then press `Enter` will introduce one. Or insert one metadata block from the menu. 

**注：快捷键 Ctrl + Shift + L 隐藏/显示侧边栏**



## Table of Contents(TOC)

输入 '[toc]' 按 enter 键会生成本文档的目录

**切换到源码模式，可以看到本文在开头添加了 `[TOC]`，用于生成本文的目录结构，且随着文章修改而自动更新**



# Span Element

## Links

Markdown 支持两种类型的 links: inline 和 reference

两种模式的链接名称都使用 [] 包含

This is [an example](https://www.baidu.com "百度一下") inline link.
[This link](https://www.baidu.com) has no title attribute.

源码：

```markdown
This is [an example](https://www.baidu.com "百度一下") inline link.
[This link](https://www.baidu.com) has no title attribute.
```

### Internal Links(内部引用)

Command(on Windows: Ctrl) + Click [This link](https://support.typora.io/Markdown-Reference/#block-elements) will jump to header `Block Elements`. To see how to write that, please move cursor or click that link with `⌘` key pressed to expand the element into markdown source. 

### Reference Links

可以先创建一个连接，[] 中的内容用一个“变量”代替，然后在本文章的任意位置均可以对该“变量”进行赋值，设置其网址和标题，如下：

This is [an example][id] reference-style link.

Then, anywhere in the document, you define your link label like this, on a line by itself:

[id]: http://example.com/  "Optional Title Here"

源码：

```markdown
This is [an example][id] reference-style link.

Then, anywhere in the document, you define your link label like this, on a line by itself:

[id]: http://example.com/  "Optional Title Here"
```

也可以将中括号内空出来，仅使用连接名称作为“变量”去赋值：

[Baidu][]

And then difine the link:

[Baidu]:http://www.baidu.com/

源码：

```markdown
[Google][]
And then define the link:
[Google]:http://google.com
```



## URLs

Typora 可以插入 URLs 作为链接，由 <> 包含

`<i@typora.io>` becomes [i@typora.io](mailto:i@typora.io). 

`<baidu>`的地址是：www.baidu.com



## Images

### 快捷键 Ctrl + Shift + I

手动编辑 `![xxx](//path)`或使用快捷键 Ctrl + Shift + I

![蓝色经典](E:\OneDrive\GitHub\Markdown-Learning\Picture\蓝色经典.jpg)

源码：

```markdown
![蓝色经典](E:\OneDrive\GitHub\Markdown-Learning\Picture\蓝色经典.jpg)
```

### 直接将图片拖进文章

此方式将自动地创建图片的链接信息

![wallhaven-133008](E:\OneDrive\GitHub\Markdown-Learning\Picture\wallhaven-133008.jpg)

源码：

```markdown
![wallhaven-133008](E:\OneDrive\GitHub\Markdown-Learning\Picture\wallhaven-133008.jpg)
```



## Emphasis

设置斜体突出显示，快捷键：Ctrl + I，或手输 `*xxx*` 或 `_xxxx_`

*single asterisks*

_single underscores_

源码:

```markdown
*single asterisks*

_single underscores_
```

**注：若需要使用`*`等特殊符号作为文本显示，则需要使用`\`对其进行转义**



## Strong

设置粗体突出显示，快捷键：Ctrl + B，或手输`**xxxx**`



## Code

`` `符号用于代码引用

**注：在行内的代码块引用使用两个`` ` 包含文本，如：**

```markdown
`code`
``code``
```



## Strikethrough

为文本添加删除线，使用`Shift` + `` `键，在文本两端添加 '~~' 符号

`Mistaken text.` becomes ~~Mistaken text~~

源码：

```markdown
`Mistaken text.` becomes ~~Mistaken text~~
```



## Underlines

为文本添加下划线：`<u>xxx</u>`

`<u>Underline</u>` becomes <u>Underline</u>.

源码：
```markdown
`<u>Underline</u>` becomes <u>Underline</u>.
```



## Emoji:happy:

`smile` -> :smile:

`satified`-> :satisfied:

......

源码：

```markdown
`smile` -> :smile:

`satified`-> :satisfied:
```



**以下功能需要开启 Markdown 扩展功能，在 Typora 中设置路径：**

**文件->偏好设置->Markdown扩展语法->全部勾选**

![Markdown扩展语法](E:\OneDrive\GitHub\Markdown-Learning\Picture\Markdown 扩展语法.png)



## Inline Math

$\lim_{x \to \infty} \exp(-x) = 0$

源码：

```
$\lim_{x \to \infty} \exp(-x) = 0$
```



## Subscript

下标设置：使用`~`包含下标文本

H~2~O

X~long~

源码：

```markdown
H~2~O

X~long~
```



## Superscript

上标设置：使用`^`包含上标文本

X^2^

源码：

```markdown
X^2^
```



## Highlight

高亮设置：使用`==`包含高亮文本

Here is the *test* of ==footnote.==

源码：

```markdown
Here is the *test* of ==footnote.==
```

