[TOC]

# Typora 标题自动编号

## 原理

​	通过修改 Typora 主题 \*.css 文件源码实现。

​	\*.css 文件位置：Typora 安装目录下 themes 文件夹下，例如 D:\Typora\themes。

​	Typora 自带的几种主题

![Typora 自带主题](E:\NS-SYN\Home-PC\File\Markdown\Typora\Picture\Typora 自带主题.bmp)

​	在该目录下分别对应，同名 \*.css 主题文件。



## 修改方法

​	使用 notepad++ 或其他文本编辑软件打开 \*.css 文件，在文本末追加 [追加代码段](#jump0)  中的代码，保存退出。重启软件即可。



## <span id="jump0">追加代码段</span>

```css
/** initialize css counter */
#write {
    counter-reset: h1
}

h1 {
    counter-reset: h2
}

h2 {
    counter-reset: h3
}

h3 {
    counter-reset: h4
}

h4 {
    counter-reset: h5
}

h5 {
    counter-reset: h6
}

/** put counter result into headings */
#write h1:before {
    counter-increment: h1;
    content: counter(h1) ". "
}

#write h2:before {
    counter-increment: h2;
    content: counter(h1) "." counter(h2) ". "
}

#write h3:before,
h3.md-focus.md-heading:before /** override the default style for focused headings */ {
    counter-increment: h3;
    content: counter(h1) "." counter(h2) "." counter(h3) ". "
}

#write h4:before,
h4.md-focus.md-heading:before {
    counter-increment: h4;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) ". "
}

#write h5:before,
h5.md-focus.md-heading:before {
    counter-increment: h5;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". "
}

#write h6:before,
h6.md-focus.md-heading:before {
    counter-increment: h6;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". "
}

/** override the default style for focused headings */
#write>h3.md-focus:before,
#write>h4.md-focus:before,
#write>h5.md-focus:before,
#write>h6.md-focus:before,
h3.md-focus:before,
h4.md-focus:before,
h5.md-focus:before,
h6.md-focus:before {
    color: inherit;
    border: inherit;
    border-radius: inherit;
    position: inherit;
    left:initial;
    float: none;
    top:initial;
    font-size: inherit;
    padding-left: inherit;
    padding-right: inherit;
    vertical-align: inherit;
    font-weight: inherit;
    line-height: inherit;
}
```



## 显示效果

​	以本文档 Typora 的 GitHub 主题为例，展示自动给标题添加标号前后效果。

**添加前：**

![添加前](E:\NS-SYN\Home-PC\File\Markdown\Typora\Picture\添加前.bmp)

**添加后：**

![添加后](E:\NS-SYN\Home-PC\File\Markdown\Typora\Picture\添加后.bmp)

​	其他主题，添加方法与之相同，不再一一示例。