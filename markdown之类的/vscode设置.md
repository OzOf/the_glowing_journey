# 编程萌新必备VSCode入门指南
> 课程内容来自B站 慕课网官方账号  
> (慕课网<https://www.imooc.com>)  
> <https://www.bilibili.com/video/BV1hw41197Ms?p=5>

跳转到[markdown中不常用的操作](#index)

## 快捷键

* CTRL + c 复制 
* CTRL + v 粘贴
* CTRL + x 剪切
* CTRL + f 查找
* CTRL + h 替换
* CTRL + / 行注释
* shift + alt + a 块注释
* CTRL + shift + enter 上方插入一行
> 上方插入一行 在我的`vscode`里的`markdown`中不管用
* CTRL + shift + f 文件夹查找
* CTRL + enter 下方插入一行
* shift + alt + f 格式化代码

## `git`是什么

* `git` 是一个开源发分布式版本控制系统
* 可以有效、高速地处理很小到非常大的项目版本管理

### git工作流

![git工作流](Screenshot/2022-01-14-16-50-05.png)

* `workspace` 正常电脑的工作区
: 直接进行标记的代码
* `repository` 本地仓库
: 本地的提交
* `remote` 远程仓库
: 盛放最终代码

1. 先要pull代码
2. 从远程仓库clone
3. 进行检出checkout
4. 本地编写代码，先添加add
5. 再提交commit
6. 没问题后push到远程仓库

### `git`下载与安装

+ 搜索git或访问<https://git-scm.com/>下载安装

### 注册`GitHub`

+ `github`是一个面向开源及私有软件项目的托管平台

# markdown中不常用操作<a id="index"></a>

## 注脚

使用 Markdown[^1]可以效率的书写文档, 直接转换成 HTML[^2]

## 超链接

### 行内式

语法说明：

- []里写链接文字,()里写链接地址, ()中的""中可以为链接指定title属性，title属性可加可不加。   
- title属性的效果是鼠标悬停在链接上会出现指定的 title文字,链接地址与title前有一个空格。

代码：
~~~
欢迎阅读 [择势勤](https://www.jianshu.com/u/16d77399d3a7 "择势量投的脸书")
~~~

显示效果：

欢迎阅读 [择势勤](https://www.jianshu.com/u/16d77399d3a7 "择势量投的脸书")

### 参考式

> 参考式超链接一般用在学术论文上面，或者另一种情况：某一个链接在文章中多处使用，那么 适合使用引用的方式创建链接，它可以让你对链接进行统一的管理。

语法说明：

- 参考式链接分为两部分
    1. 文中的写法 `[链接文字][链接标记]`
    2. 在文本的任意位置添加 `[链接标记]:链接地址。`
- 如果链接文字本身可以做为链接标记，你也可以写成  
`[链接文字][]`
`[链接文字]：链接地址`  

不同的 Markdown 应用程序处理URL中间的空格方式不一样。为了兼容性，请尽量使用%20代替空格。

代码：

        [link]
        (https://www.example.com/my%20great%20page)

~~~
我经常去的几个网站[Google][1]、[Leanote][2]、[github][]。  

[1]:http://www.google.com 
[2]:http://www.leanote.com
[github]:https://github.com/
~~~
显示效果： 

我经常去的几个网站[Google][1]、[Leanote][2]、[github][]。  

[1]:http://www.google.com 
[2]:http://www.leanote.com
[github]:https://github.com/
### 锚点（页内超链接）（只支持自定义标题）
> 网页中，锚点其实就是页内超链接，也就是链接本文档内部的某些元素，实现当前页面中的跳转。

比如我这里写下一个锚点，点击回到目录，就能跳转到目录。 在目录中点击这一节，就能跳过来。还有下一节的注脚。这些根本上都是用锚点来实现的.**只支持在标题后插入锚点，其它地方无效。**

代码：

~~~html
方法一：<!-- ！！该方法github中不可用！！-->
 # 2markdown中不常用的操作 {#index}
 文本
 文本
跳转到[markdown中不常用的操作](#index)

方法二：<!-- 该方法github中可用,
且“<a id='index'>中的 id 可换成 name” ,
而换成name后vscode中不可用，
故“显示效果”中以 id 作为示例-->
 # 2markdown中不常用的操作 <a id="index"><\a>
 文本
 文本
跳转到[markdown中不常用的操作](#index)


方法三：<!-- 该方法github中可用,
且“<a id='index'>中的 id 可换成 name” ,
而换成name后vscode中不可用--> 
 ### <a id="test2">标题2</a>
 文本
 文本
<a href="#test2">点击跳转到标题2</a>
~~~

显示效果： （方法二）

跳转到[markdown中不常用的操作](#index)

## 代码块

>代码块通常采用四个空格或一个制表符缩进。  
>当它们被放在列表中时，请将它们缩进八个空格或两个制表符。

代码：

~~~
1. 打开文件
2. 在21行找到一下代码

        <html>
          <head>
            <title>Test</title>
          </head>

3. 更新标题以匹配您网站的名称。

        include<iostream>
        using namespace std

~~~

显示效果：

1. 打开文件
2. 在21行找到一下代码

        <html>
          <head>
            <title>Test</title>
          </head>

3. 更新标题以匹配您网站的名称。

        include<iostream>
        using namespace std

## 表格

要添加表，请使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列。您可以选择在表的任一端添加管道。
~~~
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
~~~
显示效果：

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

单元格宽度可以变化，如下所示。显示效果将看起来相同。
~~~
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
~~~
Tip: 使用连字符和管道创建表可能很麻烦。为了加快该过程，请尝试使用[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables "表格生成器")。使用图形界面构建表，然后将生成的Markdown格式的文本复制到文件中。

### 对齐
可以通过在标题行中的连字符的左侧，右侧或两侧添加冒号（:），将列中的文本对齐到左侧，右侧或中心。

## 任务列表
>任务列表使您可以创建带有复选框的项目列表。在支持任务列表的Markdown应用程序中，复选框将显示在内容旁边。

要创建任务列表，请在任务列表项之前添加破折号-和方括号`[ ]`，并在`[ ]`前面加上空格。要选择一个复选框，请在方括号`[x]`之间添加 `x`。

代码：(“\- [x]”中的“\”请忽略)

~~~
\- [x] Write the press release
\- [ ] Update the website
\- [ ] Contact the media
~~~

显示效果：

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## 禁用自动URL链接

如果您不希望自动链接URL，则可以通过将URL表示为带反引号的代码来删除该链接。

~~~
`http://www.example.com`
~~~

呈现的输出如下所示：

`http://www.example.com`

[^1]:Markdown是一种纯文本标记语言
[^2]:HyperText Markup Language 超文本标记语言