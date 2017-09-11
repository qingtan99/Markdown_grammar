# Markdown的语法
> Markdown是一种增强语法，它的语法全由一些符号组成，让人一目了然，也非常容易上手；废话不多说，直接开始。

### 特殊字符自动转化

### 区块元素
#### 段落和换行
> 一个 Markdown 段落是由一个或多个连续的文本行组成，普通段落不该用空格或制表符来缩进。

#### 标题
> 类 Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题），例如：
``` 
This is an H1
=============

This is an H2
-------------
```
任何数量的 = 和 - 都可以有效果。
> 类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶，例如：
```
# 这是 H1

## 这是 H2

###### 这是 H6
```
你也可以选择性的使用类Atx的“闭合”标题，这样只是为了美观，类似这样：

```
# 这是 H1 #

## 这是 H2 ##

###### 这是 H6 ######
```

#### 区块引用 Blockquotes
> 在Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > ：
```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.
```
> 只在首行添加
```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.
```
> 区块引用可以嵌套（例如：引用内的引用）
```
> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
```
> 引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等：
```
> ## 这是一个标题。
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     return shell_exec("echo $input | $markdown_script");
```

#### 列表
> Markdown 支持有序列表和无序列表。
无序列表使用星号、加号或是减号作为列表标记：
```
*   Red
*   Green
*   Blue
```
等同于：
```
+   Red
+   Green
+   Blue
```
也等同于
```
-   Red
-   Green
-   Blue
```

有序列表则使用数字接着一个英文句点：
```
1.  Bird
2.  McHale
3.  Parish
```
#### 代码区块
> 在markdown中建立代码区块其实很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以，例如，下面的输入：
```
这是一个普通段落：

    这是一个代码区块。
```
Markdown 会转换成：
```
<p>这是一个普通段落：</p>

<pre><code>这是一个代码区块。
</code></pre>
```

> 在代码区块里面， & 、 < 和 > 会自动转成 HTML 实体，这样的方式让你非常容易使用 Markdown 插入范例用的 HTML 原始码，只需要复制贴上，再加上缩进就可以了，剩下的 Markdown 都会帮你处理，例如：
```
<div class="footer">
        &copy; 2004 Foo Corporation
    </div>
```
会被转换为：
```
<pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Foo Corporation
&lt;/div&gt;
</code></pre>
```

#### 分割线
> 你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

```
* * *

***

*****

- - -

-----------
```

### 区段元素
#### 链接
> Markdown 支持两种形式的链接语法： 内联和引用两种方式。
```
内联方式：This is an [example link](http://example.com/)
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].  

[1]: http://google.com/        "Google" 
[2]: http://search.yahoo.com/  "Yahoo Search" 
[3]: http://search.msn.com/    "MSN Search"
```

#### 图片
> Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种方式： 行内式和参考式。
```
行内式式：![alt text](/path/to/img.jpg "Title")
参考式：
![alt text][id] 

[id]: /path/to/img.jpg "Title"
```

#### 强调
> Markdown 使用星号（*）和和底线（_）作为标记强调字词的符号，用两个包起来使用，是使字体加粗
```
*single asterisks*

_single underscores_

**double asterisks**

__double underscores__
```

#### 代码
```
1. 简单文字出现一个代码框。使用`<blockquote>`。（`不是单引号而是左上角的ESC下面~中的`）
2. 大片文字需要实现代码框。使用Tab和四个空格。
