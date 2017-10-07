title: Markdown语法测试
tags:
  - Markdown
---
这是我的第一篇博客，试试Markdown语法而已

Setext形式标题1
===
Setext形式标题2
---

# atx 形式标题 1
## atx 形式标题 2
### atx 形式标题 3
#### atx 形式标题 4
##### atx 形式标题 5
###### atx 形式标题 6

# 区块代码
> This is a blockquote.
> This is the second paragraph in the blockquote.
> # This is an H1 in a blockquote
> ## This is an H2 in a blockquote
> ### This is an H3 in a blockquote
> #### This is an H4 in a blockquote
> ##### This is an H5 in a blockquote
> ###### This is an H6 in a blockquote
>> ???
>>> ???
>>>>> ???

# 修辞和强调
Some of these words *are emphasized*.
Some of these words _are emphasized also_.
Use two asterisks for **strong emphasis**.
Or, if you prefer, __use two underscores instead__.

# 列表
* Candy.
* Gum.
* Booze.
+ Candy.
+ Gum.
+ Booze.
- Candy.
- Gum.
- Booze.
1. Red
2. Green
3. Blue

# 链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。
不管是哪一种，链接文字都是用 [方括号] 来标记。
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：
This is an [example link](http://example.com/).
This is an [example link](http://example.com/ "With a Title").
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
I start my morning with a cup of coffee and [The New York Times][NY Times].
[1]: http://google.com/ "Google"
[2]: http://search.yahoo.com/ "Yahoo Search"
[3]: http://search.msn.com/ "MSN Search"
[ny times]: http://www.nytimes.com/
## 自动链接
<http://example.com/>

# 图片
## 行内形式（title 是选择性的）
![alt text](/../image.jpg "Title")
## 参考形式
![alt text][id]
[id]: /../image.jpg "Title"

# 代码
## 段内代码
在一般的段落文字中，你可以使用反引号 \` 来标记代码区段，区段内的 &、< 和 > 都会被自动的转换成 HTML 实体，这项特性让你可以很容易的在代码区段内插入 HTML 码
I strongly recommend against using any `<blink>` tags.
I wish SmartyPants used named entities like `&mdash;`
instead of decimal-encoded entites like `&#8212;`.
## 代码区块
如果要建立一个已经格式化好的代码区块，只要每行都缩进 4 个空格或是一个 tab 就可以了，而 &、< 和 > 也一样会自动转成 HTML 实体。
Markdown 语法:
    int main
失灵了，不好用
## 语言代码标识
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
```c
#include<stdio.h>
int main()
{
	printf("hello world");
	return 0;
}
```

# NexT内置标签
## 文本居中的引用
<!-- HTML方式: 直接在 Markdown 文件中编写 HTML 来调用 -->
<!-- 其中 class="blockquote-center" 是必须的 -->
<blockquote class="blockquote-center">blah blah blah</blockquote>
<!-- 标签 方式，要求版本在0.4.5或以上 -->
{% centerquote %}blah blah blah{% endcenterquote %}
<!-- 标签别名 -->
{% cq %} blah blah blah {% endcq %}

## 突破容器宽度限制的图片
<!-- HTML方式: 直接在 Markdown 文件中编写 HTML 来调用 -->
<!-- 其中 class="full-image" 是必须的 -->
<img src="/image-url" class="full-image" />
<!-- 标签 方式，要求版本在0.4.5或以上 -->
{% fullimage /../image.jpg, alt, title %}
<!-- 别名 -->
{% fi /../image.jpg, alt, title %}

## Bootstrap Callout
{% note default %} default {% endnote %}
{% note primary %} primary {% endnote %}
{% note success %} success {% endnote %}
{% note info %} info {% endnote %}
{% note warning %} warning {% endnote %}
{% note danger %} danger {% endnote %}

# 参考网址
[Markdown: Basics （快速入门）](http://www.appinn.com/markdown/basic.html)
[NexT 内置标签](http://theme-next.iissnan.com/tag-plugins.html)