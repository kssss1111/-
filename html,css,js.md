# 一、VScode开发者工具快捷键

![image-20211122160106255](https://www.itbaizhan.com/wiki/imgs/image-20211122160106255.png)

**VSCode打开文件夹与创建文件**

1. 选择文件夹
2. 拖拽文件夹

生成浏览器文件`.html`的快捷方式

```html
! + 回车
```

**VSCode常用快捷键列表**

1. 代码格式化：`Shift+Alt+F`
2. 向上或向下移动一行：`Alt+Up 或 Alt+Down`
3. 快速复制一行代码：`Shift+Alt+Up 或 Shift+Alt+Down`
4. 快速保存：`Ctrl + S`
5. 快速查找：`Ctrl + F`
6. 快速替换：`Ctrl + H`

**实时效果反馈**

**1. VSCode快速复制一行代码的快捷键是：**

A Shift+Alt+F

B Ctrl + S

C Alt+Up 或 Alt+Down

D Shift+Alt+Up 或 Shift+Alt+Down

**2. VSCode快速移动一行代码快捷键:**

A Shift+Alt+F

B Ctrl + S

C Alt+Up 或 Alt+Down

D Shift+Alt+Up 或 Shift+Alt+Down

**答案**

1=>D 2=>C

#  二、HTML5简介与基础骨架

![image-20211017170903615](https://www.itbaizhan.com/wiki/imgs/image-20211017170903615.png)

## I、HTML5介绍

HTML5是用来描述网页的一种语言，被称为超文本标记语言。用HTML5编写的文件，后缀以`.html`结尾

HTML是一种标记语言，标记语言是一套标记标签。标签是由尖括号包围的关键字，例如：`<html>`

标签有两种表现形式：

1. 双标签，例如：`<html></html>`
2. 单标签，例如：`<img>`

### 1、HTML5的DOCTYPE声明

DOCTYPE是`document type` (文档类型) 的缩写。`<!DOCTYPE html >`是H5的声明位于文档的最前面，处于标签之前。 他是网页必备的组成部分，避免浏览器的怪异模式。

```html
<!DOCTYPE html>
```

![image-20211014164839770](https://www.itbaizhan.com/wiki/imgs/image-20211014164839770.png)

### 2、HTML5基本骨架

![image-20211014164952540](https://www.itbaizhan.com/wiki/imgs/image-20211014164952540.png)

#### html标签

定义 HTML 文档，这个元素我们浏览器看到后就明白这是个HTML文档了，所以你的其它元素要包裹在它里面，标签限定了文档的开始点和结束点。

```html
<!DOCTYPE html>
<html>
</html>
```

#### head标签

head标签用于定义文档的头部。文档的头部描述了文档的各种属性和信息，包括文档的标题、在 Web 中的位置以及和其他文档的关系等。绝大多数文档头部包含的数据都不会真正作为内容显示给读者。

```html
<!DOCTYPE html>
<html>
    <head>
    </head>
</html>
```

#### body标签

body 元素定义文档的主体。

body 元素包含文档的所有内容（比如文本、超链接、图像、表格和列表等等。）

它会直接在页面中显示出来，也就是用户可以直观看到的内容

```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        我会显示在浏览器中
    </body>
</html>
```

#### title标签

1. 可定义文档的标题。
2. 它显示在浏览器窗口的标题栏或状态栏上。
3. `<title>` 标签是 `<head>` 标签中唯一必须要求包含的东西，就是说写head一定要写title
4. `<title>`的增加有利于SEO优化

> SEO是搜索引擎优化的英文缩写。通过对网站内容调整，满足搜索引擎的排名需求

```html
<!DOCTYPE html>
<html>
    <head>
        <title>第一个页面</title>
    </head>
    <body>
        我会显示在浏览器中
    </body>
</html>
```

#### meta标签

meta标签用来描述一个HTML网页文档的属性，关键词等，例如：`charset="utf-8"`是说当前使用的是`utf-8`编码格式，在开发中我们经常会看到`utf-8`，或是`gbk`，这些都是编码格式，通常使用`utf-8`。

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>itbaizhan</title>
    </head>
    <body>
    </body>
</html>
```

**实时效果反馈**

**1. 下列哪些标签书写格式是正确的是：**

A 《html》

B <!html>

C html

D `<html>`

**2. 以下组成HTML5基础骨架标签正确的是:**

A `<html>、<body>、<head>、<div>、<meta>`

B `<html>、<body>、<DOCTYPE>、<title>、<meta>`

C `<html>、<body>、<head>、<title>、<meta>`

D `<html>、<body>、<!DOCTYPE html>、<title>、<meta>`

**答案**

1=>D 2=>C

##  II、标签之标题

![image-20211120171417126](https://www.itbaizhan.com/wiki/imgs/image-20211120171417126.png)

### 标题介绍与应用

标题（Heading）是通过 `<h1> - <h6>`标签进行定义的。

`<h1>`定义最大的标题 `<h6>`定义最小的标题

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```

> 生成h1~h6快捷键：h$*6

### VSCode插件

快速打开浏览器

扩展 -> 搜索open in browser -> 点击安装

**正确使用标题**

请确保将 HTML 标题标签只用于标题。

不要仅仅是为了生成粗体或大号的文本而使用标题。

正确使用标题有益于SEO

应该将`< h1>` 用作主标题（最重要的），其后是 `<h2>`（次重要的），再其次是 `<h3>`，以此类推

![image-20211014171609998](https://www.itbaizhan.com/wiki/imgs/image-20211014171609998.png)

**标题标签位置摆放**

在标签中添加属性：`align="left | center | right"` 默认居左

![image-20211017140517014](https://www.itbaizhan.com/wiki/imgs/image-20211017140517014.png)



**实时效果反馈**

**1. 以下那个是三级标题标签：**

A `<h1></h1>`

B `<h2></h2>`

C `<h3></h3>`

D `<h4></h4>`

**2. 标题标签居中摆放属性使用正确的是:**

A `align="left | center | right"`

B `align="left"`

C `align="center"`

D `align="right"`

**答案**

1=>C 2=>C

##  III、标签之段落、换行、水平线

![image-20211120171852680](https://www.itbaizhan.com/wiki/imgs/image-20211120171852680.png)

### 1、标签之段落

段落是通过`<p>`标签定义的

```html
<p>这是一个段落 </p> 
<p>这是另一个段落</p>
```

![image-20211017125215977](https://www.itbaizhan.com/wiki/imgs/image-20211017125215977.png)

### 2、换行

如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 `<br>`

`<br />` 元素是一个空的 HTML 元素。

```html
<p>这个<br>段落<br>演示了分行的效果</p>
```

![image-20211014175748915](https://www.itbaizhan.com/wiki/imgs/image-20211014175748915.png)

### 3、水平线

`<hr/>`标签在 HTML 页面中创建水平线

```html
<hr color="" width="" size="" align=""/>
```

属性：

1. color：设置水平线的颜色
2. width：设置水平线的宽度
3. size：设置水平线的高度
4. align：设置水平线的对齐方式（默认居中），可取值left|right

**实时效果反馈**

**1. 要实现一个文本换行，可以使用以下那个标签：**

A `<p>`标签

B `<hr>`标签

C `<br>`标签

D `<img>`标签

**2. 承载段落文本信息使用以下那个标签:**

A `<p>`标签

B `<hr>`标签

C `<br>`标签

D `<img>`标签

**答案**

1=>C 2=>A

##  IV、图片路径详解

![image-20211120172729161](https://www.itbaizhan.com/wiki/imgs/image-20211120172729161.png)

### 绝对路径

绝对路径是电脑的盘符存储与访问的具体地址

```html
E:\itbaizhanCode\1.jpg
<img src="E:\itbaizhanCode\1.jpg">
```

### 相对路径

两者相对关系，两者在同⼀路径下可以直接访问

1. 子级关系: `/`
2. 父级关系: `../`
3. 同级关系: `./`（可以省略）

### 网络路径

具体的⽹络地址: http://iwenwiki.com/api/newworld/images/n1.png

**实时效果反馈**

**1. 以下那个是相对路径：**

A `E:\itbaizhanCode\1.jpg`

B `http://iwenwiki.com/api/newworld/images/n1.png`

C `../images/1.jpg`

D `C:\itbaizhanCode\2.jpg`

**2. 以下关于相对路径描述正确的是：**

A 相对路径是电脑的盘符存储与访问的具体地址

B 相对路径是两者相对关系，两者在同⼀路径下可以直接访问

C 相对路径是具体的⽹络地址

D 相对路径是不存在的

**答案**

1=>C 2=>B

##  V、标签之超文本链接

![image-20211120173236840](https://www.itbaizhan.com/wiki/imgs/image-20211120173236840.png)

### 1、超链接描述

HTML使用标签 `<a>`来设置超文本链接

超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档

```html
<a href="url">链接文本</a>
```

### 2、超链接属性

在标签`<a>`中使用了`href`属性来描述链接的地址

默认情况下，链接将以，以下形式出现在浏览器中：

1. 一个未访问过的链接显示为蓝色字体并带有下划线。
2. 访问过的链接显示为紫色并带有下划线。
3. 点击链接时，链接显示为红色并带有下划线。

> **特别提示**
>
> 后期我们会通过CSS样式修改掉这些效果

### 3、超链接表现

当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手

![image-20211017141221711](https://www.itbaizhan.com/wiki/imgs/image-20211017141221711.png)

**实时效果反馈**

**1. 超链接的作用是**

A 跳转到新的文档

B 显示图片的标签

C 显示段落的标签

D 显示标题的标签

**2. 超链接中`href`属性的作用**

A 设置超链接的宽度和高度

B 设置超链接的跳转地址

C 设置超链接的显示颜色

D 设置超链接的文本内容

**答案**

1 =>A 2=>B

##  VI、标签之文本

![image-20211120173736274](https://www.itbaizhan.com/wiki/imgs/image-20211120173736274.png)

### 1、常用文本标签

|    标签    |        描述        |
| :--------: | :----------------: |
|   `<em>`   |    定义着重文字    |
|   `<b>`    |    定义粗体文本    |
|   `<i>`    |     定义斜体字     |
| `<strong>` |    定义加重语气    |
|  `<del>`   |     定义删除字     |
|  `<span>`  | 元素没有特定的含义 |

> **特别提示**
>
> 常用文本标签和段落是不同的，段落代表一段文本，而文本标签一般表示文本词汇

**实时效果反馈**

**1. 定义加重语气的标签是哪一个：**

A `em`

B `<i>`

C `<del>`

D `<strong>`

**2. 定义着重文字的标签是哪一个：**

A `em`

B `<i>`

C `<del>`

D `<strong>`

**答案**

1=>D 2=>A

##  VII、列表标签之有序列表

![image-20211120174415921](https://www.itbaizhan.com/wiki/imgs/image-20211120174415921.png)

### 1、有序列表

有序列表是一列项目，列表项目使用数字进行标记。 有序列表始于`<ol>` 标签。每个列表项始于 `<li>`标签。

```html
<ol>
    <li>尚学堂</li>
    <li>百战程序员</li>
</ol>
```

![image-20211017132005211](https://www.itbaizhan.com/wiki/imgs/image-20211017132005211.png)

### type属性

`<ol>`的属性type 拥有的选项

1. 1 表示列表项目用数字标号（1,2,3...）
2. a 表示列表项目用小写字母标号（a,b,c...）
3. A 表示列表项目用大写字母标号（A,B,C...）
4. i 表示列表项目用小写罗马数字标号（i,ii,iii...）
5. I 表示列表项目用大写罗马数字标号（I,II,III...）

### 有序列表嵌套

列表是可以进行嵌套的

```html
<ol>
    <li>尚学堂</li>
    <li>
        <ol>
            <li>阿里</li>
            <li>京东</li>
        </ol>
    </li>
    <li>百战程序员</li>
</ol>
```

**实时效果反馈**

**1. 有序列表展示效果以下那个描述是正确的：**

A 展示一个段落效果

B 展示一个无序的列表效果

C 展示一个有序的列表效果

D 展示一个加粗的文本效果

**2. 有序列表的标签组合正确的是：**

A `<ul> + <li>`

B `<ol> + <li>`

C `<h1> + <li>`

D `<img> + <li>`

**答案**

1=>C 2=>B

##  VIII、列表标签之无序列表

![image-20211120174927373](https://www.itbaizhan.com/wiki/imgs/image-20211120174927373.png)

### 1、无序列表实现

无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记

无序列表始于 `<ul>` 标签。每个列表项始于`<li>` 标签。

```html
<ul>
    <li>尚学堂</li>
    <li>百战程序员</li>
</ul>
```

### 2、type属性

`<ul>`的属性type 拥有的选项

- disc 默认实心圆
- circle 空心圆
- square 小方块
- none 不显示

### 3、无序列表嵌套

列表是可以进行嵌套的

```html
<ul>
    <li>尚学堂</li>
    <li>
        <ul>
            <li>阿里</li>
            <li>京东</li>
        </ul>
    </li>
    <li>百战程序员</li>
</ul>
```

### 4、常见应用场景

1. 无序的列表效果
2. 导航效果

### 5、导航效果

```html
<ul>
    <li>Xiaomi手机</li>
    <li>Redmi 红米</li>
    <li>电视</li>
    <li>笔记本</li>
</ul>
```

![image-20211016124431658](https://www.itbaizhan.com/wiki/imgs/image-20211016124431658.png)

> **快捷键**
>
> 快速生成ul+li的布局：ul>li*3（数字根据自己的需要的li数量修改）

**实时效果反馈**

**1. 无序列表的type属性以下描述错误的是：**

A disc 默认实心圆

B circle 空心圆

C square 小方块

D triangle 三角形

**2. 无序列表的标签组合正确的是：**

A `<ul> + <li>`

B `<ol> + <li>`

C `<h1> + <li>`

D `<img> + <li>`

**答案**

1=>D 2=>A

##  IX、标签之表格

![image-20211120180329440](https://www.itbaizhan.com/wiki/imgs/image-20211120180329440.png)

### 1、表格展示效果

表格在数据展示方面非常简单，并且表现优秀

![image-20211016145021813](https://www.itbaizhan.com/wiki/imgs/image-20211016145021813.png)

> **表格组成与特点**
>
> 行、列、单元格
>
> 单元格特点：同行等高、同列等宽。
>
> ------
>
> **表格标签**
>
> 表格：`<table>`
>
> 行：`<tr>`
>
> 单元格(列)：`<td>`

```html
<table>
    <tr>
        <td>尚学堂</td>
        <td>百战程序员</td>
    </tr>
    <tr>
        <td>阿里</td>
        <td>京东</td>
    </tr>
</table>
```

> **快捷键**
>
> 快速生成表格结构：table>tr*2>td{单元格}

### 2、表格属性

1. border：设置表格的边框
2. width：设置表格的宽度
3. height：设置表格的高度

**实时效果反馈**

**1. 以下那个是表格组成标签组合：**

A table + tr + td

B table + tr + dl

C ul + tr + td

D ul + table + tr

**2. 以下代码，空格处要填写的标签：**

```html
<table>
    ___
        <td>尚学堂</td>
        <td>百战程序员</td>
    ___
</table>
```

A `<th>` `</th>`

B `<tbody>` `</tbody>`

C `<td>` `</td>`

D `<tr>` `</tr>`

**答案**

1=>A 2=>D

##  X、表格单元格合并

![image-20211124111834625](https://www.itbaizhan.com/wiki/imgs/image-20211124111834625.png)

### 单元格合并属性

![image-20211124133917914](https://www.itbaizhan.com/wiki/imgs/image-20211124133917914.png)

- 水平合并：colspan
- 垂直合并：rowspan

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>合并6，7单元格</p>
    <p>合并15，20单元格</p>
    <p>合并13，18,23单元格</p>
    <p>合并16，17,21,22单元格</p>
    <p>水平合并：保留左边，删除右边</p>
    <p>垂直合并：保留上边，删除下边</p>

    <table border="1" width="600px" height="400px">
        <tr>
            <td>单元格1</td>
            <td>单元格2</td>
            <td>单元格3</td>
            <td>单元格4</td>
            <td>单元格5</td>
        </tr>
        <tr>
            <td colspan="2">单元格6,7</td>
            <td>单元格8</td>
            <td>单元格9</td>
            <td>单元格10</td>
        </tr>
        <tr>
            <td>单元格11</td>
            <td>单元格12</td>
            <td rowspan="3">单元格13,18,23</td>
            <td>单元格14</td>
            <td rowspan="2">单元格15,20</td>
        </tr>
        <tr>
            <td colspan="2" rowspan="2">单元格16,17,21,22</td>
            <td>单元格19</td>
        </tr>
        <tr>
            <td>单元格24</td>
            <td>单元格25</td>
        </tr>
    </table>
</body>
</html>
```

**实时效果反馈**

**1. 下列那个是单元格垂直合并的属性：**

A border

B align

C colspan

D rowspan

**答案**

1=>D

## XI、Form表单

![image-20211124172703466](https://www.itbaizhan.com/wiki/imgs/image-20211124172703466.png)

表单在 Web 网页中用来给用户填写信息，从而能采用户信息，使网页具有交互的功能。

所有的用户输入内容的地方都用表单来写，如登录注册、搜索框

![image-20211124143834115](https://www.itbaizhan.com/wiki/imgs/image-20211124143834115.png)

表单是由容器和控件组成的,一个表单一般应该包含用户填写信息的输入框,按钮等，这些输入框,按钮叫做控件,表单就是容器,它能够容纳各种各样的控件

```html
<form action="url" method="get|post" name="myform"></form>
```

> **属性说明**
>
> action服务器地址
>
> name表单名称
>
> **method中Get和Post的区别**
>
> 1. 数据提交方式，get把提交的数据url可以看到，post看不到
> 2. get一般用于提交少量数据，post用来提交大量数据

### 1、表单元素

一个完整的表单包含三个基本组成部分：表单标签、表单域、表单按钮

1. 表单标签
2. 表单域
3. 表单按钮

```html
<form>
    <input type="text">
    <input type="submit">
</form>
```

**实时效果反馈**

**1.以下哪个元素不是表单元素：**

A 表单标签

B 表单域

C 表单按钮

D 图片

**答案**

1=>D

 **表单元素**

![image-20211124173247447](https://www.itbaizhan.com/wiki/imgs/image-20211124173247447.png)

### 2、文本框

文本域通过`<input type="text">` 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域

```html
<form>
    First name: <input type="text" name="firstname">
    <br>
    Last name: <input type="text" name="lastname">
</form>
```

![image-20211124145315178](https://www.itbaizhan.com/wiki/imgs/image-20211124145315178.png)

### 3、密码框

密码字段通过标签`<input type="password">` 来定义

```html
<form>
    Password: <input type="password" name="pwd">
</form>
```

![image-20211124145447289](https://www.itbaizhan.com/wiki/imgs/image-20211124145447289.png)

> **温馨提示**
>
> 密码字段字符不会明文显示，而是以星号或圆点替代

### 4、提交按钮

当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理

```html
<form name="input" action="url" method="get">
    Username: <input type="text" name="user">
    <input type="submit" value="Submit">
</form>
```

复制

![image-20211124150330131](https://www.itbaizhan.com/wiki/imgs/image-20211124150330131.png)

**实时效果反馈**

**1.设置输入框为密码框，type属性应该填写内容：**

A text

B password

C radio

D name

**答案**

1=>B

##  XII、块元素与行内元素（内联元素）

![image-20211126104646087](https://www.itbaizhan.com/wiki/imgs/image-20211126104646087.png)

HTML5出现之前，经常把元素按照块级元素和内联元素来区分。在HTML5中，元素不再按照这种⽅式来区分， 而是按照内容模型来区分，分为元数据型(metadata content)、区块型(sectioning content)、标题型(heading content)、文档流型(flow content)、语句型(phrasing content)、内嵌型(embedded content)、交互型 (interactive content)。元素不属于任何⼀个类别，被称为穿透的，元素可能属于不止⼀个类别，称为混合的

![Content_categories_venn](https://www.itbaizhan.com/wiki/imgs/Content_categories_venn.png)

详细参考地址：https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/Content_categories

虽然到了HTML5的版本，元素分类更细致了，但是这对初学者并不友好,所以我们仍然按照块元素和内联元素做区分，这对我们的布局起到了至关重要的作用

内联元素和块级元素的区别

|                   块级元素                   |                   内联元素                   |
| :------------------------------------------: | :------------------------------------------: |
| 块元素会在页面中独占一行（自上向下垂直排列） | 行内元素不会独占页面中的一行，只占自身的大小 |
|          可以设置width，height属性           |      行内元素设置width，height属性无效       |
|  ⼀般块级元素可以包含行内元素和其他块级元素  |    ⼀般内联元素包含内联元素不包含块级元素    |

常见块级元素

> div、form、h1~h6、hr、p、table、ul、等

常见内联元素(行内元素)

> a、b、em、i、span、strong等

行内块级元素（特点：不换行、能够识别宽高）

> button、img、input等

**实时效果反馈**

**1.下列关于元素分类描述错误的是：**

A 块元素会在页面中独占一行,行内元素不会独占页面中的一行，只占自身的大小

B 块元素可以设置width，height属性,行内元素设置width，height属性无效

C ⼀般块级元素可以包含行内元素和其他块级元素,⼀般内联元素包含内联元素不包含块级元素

D 块元素可以设置大小,不会独占一行,行内元素无法无法设置大小,但是会独占一行

**答案**

1=>D

##  XIII、HTML5新增标签

![image-20211126170309621](https://www.itbaizhan.com/wiki/imgs/image-20211126170309621.png)

`HTML5`是`HTML`最新的修订版本，2014年10月由万维网联盟`（W3C）`完成标准制定

在`HTML5`出现之前，我们一般采用`DIV+CSS`布局我们的页面。但是这样的布局方式不仅使我们的文档结构不够清晰，而且**不利于搜索引擎爬虫对我们页面的爬取**。为了解决上述缺点，`HTML5`新增了很多新的语义化标签

## XIV、扩展知识

`div`容器元素，也是页面中见到的最多的元素

div实现

![image-20211126150749756](https://www.itbaizhan.com/wiki/imgs/image-20211126150749756.png)

H5新标签实现

![image-20211126150757403](https://www.itbaizhan.com/wiki/imgs/image-20211126150757403.png)

**H5新标签**

1. `<header></header>` 头部
2. `<nav></nav>` 导航
3. `<section></section>`定义文档中的节,比如章节、页眉、页脚
4. `<aside></aside>` 侧边栏
5. `<footer></footer>` 脚部
6. `<article></article>` 代表一个独立的、完整的相关内容块,例如一篇完整的论坛帖子，一篇博客文章，一个用户评论等

**实时效果反馈**

**1.下列哪个不属于HTML5的新增标签**

A `<header></header>`

B `<div></div>`

C `<footer></footer>`

D `<nav></nav>`

**答案**

1=>B

# 三、CSS简介

![image-20211130110019853](https://www.itbaizhan.com/wiki/imgs/image-20211130110019853.png)

## I、CSS概念

CSS（Cascading Style Sheets）层叠样式表，又叫级联样式表，简称样式表

CSS文件后缀名为`.css`

CSS用于HTML文档中元素样式的定义

### 为什么需要CSS

使用css的唯一目的就是让网页具有美观一致的页面

### 语法

CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明（样式）

![image-20211129154503132](https://www.itbaizhan.com/wiki/imgs/image-20211129154503132.png)

选择器通常是您需要改变样式的 HTML 元素

每条声明由一个属性和一个值组成

属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开

```css
<style>
    h1{
        color: blue;
        font-size: 12px;
    }
</style>

```

**实时效果反馈**

**1.下列关于CSS基础语法描述错误的是：**

A CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明

B 选择器通常是您需要改变样式的 HTML 元素

C 每条声明由一个属性和一个值组成

D 属性与属性值之间用分号隔开

**答案**

1=>D

##  II、CSS的引入方式

![image-20211130111128496](https://www.itbaizhan.com/wiki/imgs/image-20211130111128496.png)

### 内联样式（行内样式）

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性

> **温馨提示**
>
> 缺乏整体性和规划性，不利于维护，维护成本高

```css
<p style="background: orange; font-size: 24px;">CSS<p>
```

### 内部样式

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 `<style>` 标签在文档头部定义内部样式表

> **温馨提示**
>
> 单个页面内的CSS代码具有统一性和规划性，便于维护，但是在多个页面之间容易混乱

```css
<head>
    <style> 
       h1 { 
           background: red; 
       } 
    </style>
</head>

```

### 外部样式（推荐）

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 `<link>` 标签链接到样式表。 `<link>` 标签在（文档的）头部

```css
<link rel="stylesheet" type="text/css" href="xxx.css">
```

**实时效果反馈**

**1.外部CSS样式的引入方式，以下正确的是：**

A `<style></style>`

B `<link rel="stylesheet" href="xxx.css">`

C `<p style="background: orange; font-size: 24px;">CSS<p>`

**答案**

1=>B

##  III、选择器一

![image-20211130113235236](https://www.itbaizhan.com/wiki/imgs/image-20211130113235236.png)

CSS语法 规则由两个主要的部分构成：**选择器**，以及一条或多条声明（样式）

### 全局选择器

可以与任何元素匹配，优先级最低，一般做样式初始化

```css
*{
     margin: 0;
     padding: 0;
 }

```

### 元素选择器

HTML文档中的元素，`p、b、div、a、img、body`等。

标签选择器，选择的是页面上所有这种类型的标签，所以经常描述“共性”，无法描述某一个元素的“个性”

```css
p{
    font-size:14px;
}

```

再比如说，我想让“学完前端，继续学Java”这句话中的“前端”两个变为红色字体，那么我可以用`<span>`标签把“前端”这两个字围起来，然后给`<span>`标签加一个标签选择器

```css
<p>学完了<span>前端</span>，继续学Java</p>
span{
    color: red;
}

```

> **温馨提示**
>
> 1. 所有的标签，都可以是选择器。比如ul、li、label、dt、dl、input、div等
> 2. 无论这个标签藏的多深，一定能够被选择上
> 3. 选择的所有，而不是一个

### 类选择器

规定用圆点 `.` 来定义，针对你想要的所有标签使用

> **优点**
>
> 灵活

```css
<h2 class="oneclass">你好</h2>
/*定义类选择器*/
.oneclass{
    width:800px;
}

```

> **class属性的特点**
>
> 1. 类选择器可以被多种标签使用
> 2. 类名不能以数字开头
> 3. 同一个标签可以使用多个类选择器。用空格隔开

```css
<h3 class="classone  classtwo">我是一个h3啊</h3>
<h3 class="teshu" class="zhongyao">我是一个h3啊</h3>  // 错误
```

**实时效果反馈**

**1.下列代码哪个是类选择器使用方式：**

A `h1{color:red;}`

B `*{margin:0;}`

C `.title{color:red;}`

D `h3{color:red;}`

**答案**

1=>C

##  IV、选择器二

![image-20211130113629959](https://www.itbaizhan.com/wiki/imgs/image-20211130113629959.png)

### ID选择器

针对某一个特定的标签来使用，只能使用一次。`css`中的`ID选择器`以 `#` 来定义

```css
<h2 id="mytitle">你好</h2>
#mytitle{
    border:3px dashed green;
}

```

> **特别强调**
>
> 1. ID是唯一的
> 2. ID不能以数字开头

### 合并选择器

语法：`选择器1,选择器2,...{ }`

作用：提取共同的样式，减少重复代码

```css
.header, .footer{
    height:300px;
}

```

### 选择器的优先级

CSS中,权重用数字衡量

元素选择器的权重为: 1

class选择器的权重为: 10

id选择器的权重为: 100

内联样式的权重为: 1000

优先级从高到低: 行内样式 > ID选择器 > 类选择器 > 元素选择器

**实时效果反馈**

**1.下列选择器优先级排序正确的是：**

A 行内样式 > ID选择器 > 类选择器 > 元素选择器

B 行内样式 > 类选择器 > ID选择器 > 元素选择器

C 行内样式 > 元素选择器 > 类选择器 > ID选择器

D 元素选择器 > ID选择器 > 类选择器 > 行内样式

**答案**

1=>A

##  V、字体属性

![image-20211201102751858](https://www.itbaizhan.com/wiki/imgs/image-20211201102751858.png)

CSS字体属性定义字体，颜色、大小，加粗，文字样式

### color

规定文本的颜色

```css
div{ color:red;}
div{ color:#ff0000;}
div{ color:rgb(255,0,0);}
div{ color:rgba(255,0,0,.5);}

```

### font-size

设置文本的大小

能否管理文字的大小，在网页设计中是非常重要的。但是，你不能通过调整字体大小使段落看上去像标题，或者使标题看上去像段落。

```css
h1 {font-size:40px;}
h2 {font-size:30px;}
p {font-size:14px;}

```

> **温馨提示**
>
> chrome浏览器接受最小字体是12px

### font-weight

设置文本的粗细

| 值      | 描述                                      |
| ------- | ----------------------------------------- |
| bold    | 定义粗体字符                              |
| bolder  | 定义更粗的字符                            |
| lighter | 定义更细的字符                            |
| 100~900 | 定义由细到粗 400等同默认，而700等同于bold |

```css
H1 {font-weight:normal;}
div{font-weight:bold;}
p{font-weight:900;}

```

### font-style

指定文本的字体样式

| 值     | 描述       |
| ------ | ---------- |
| normal | 默认值     |
| italic | 定义斜体字 |

### font-family

font-family属性指定一个元素的字体

> **温馨提示**
>
> 每个值用逗号分开
>
> 如果字体名称包含空格，它必须加上引号

```css
font-family:"Microsoft YaHei","Simsun","SimHei";
```

**实时效果反馈**

**1.下列哪个属性可以设置字体粗细：**

A font-family

B font-style

C font-weight

D font-size

**答案**

1=>C

##  VI、背景属性

![image-20211201103919909](https://www.itbaizhan.com/wiki/imgs/image-20211201103919909.png)

CSS背景属性主要有以下几个

| 属性                | 描述                 |
| ------------------- | -------------------- |
| background-color    | 设置背景颜色         |
| background-image    | 设置背景图片         |
| background-position | 设置背景图片显示位置 |
| background-repeat   | 设置背景图片如何填充 |
| background-size     | 设置背景图片大小属性 |

### background-color属性

该属性设置背景颜色

```css
<div class="box"></div>
.box{
    width: 300px;
    height: 300px;
    background-color: palevioletred;
}

```

### background-image属性

设置元素的背景图像

元素的背景是元素的总大小，包括填充和边界（不包括外边距）。默认情况下background-image属性放置在元素的左上角，如果图像不够大的话会在垂直和水平方向平铺图像，如果图像大小超过元素大小从图像的左上角显示元素大小的那部分

```css
<div class="box"></div>
.box{
    width: 600px;
    height: 600px;
    background-image: url("images/img1.jpg");
}

```

### background-repeat属性

该属性设置如何平铺背景图像

| 值        | 说明             |
| --------- | ---------------- |
| repeat    | 默认值           |
| repeat-x  | 只向水平方向平铺 |
| repeat-y  | 只向垂直方向平铺 |
| no-repeat | 不平铺           |

```css
.box{
    width: 600px;
    height: 600px;
    background-color: #fcc;
    background-image: url("images/img1.jpg");
    background-repeat: no-repeat;
}

```

### background-size属性

该属性设置背景图像的大小

| 值         | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| length     | 设置背景图片的宽度和高度，第一个值宽度，第二个值高度，如果只是设置一个，第二个值auto |
| percentage | 计算相对位置区域的百分比，第一个值宽度，第二个值高度，如果只是设置一个，第二个值auto |
| cover      | 保持图片纵横比并将图片缩放成完全覆盖背景区域的最小大小       |
| contain    | 保持图片纵横比并将图像缩放成适合背景定位区域的最大大小       |

```css
.box{
    width: 600px;
    height: 600px;
    background-image: url("images/img1.jpg");
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

```

### background-position属性

该属性设置背景图像的起始位置，其默认值是：0% 0%

| 值            | 说明                                                         |
| ------------- | ------------------------------------------------------------ |
| left top      | 左上角                                                       |
| left center   | 左 中                                                        |
| left bottom   | 左 下                                                        |
| right top     | 右上角                                                       |
| right center  | 右 中                                                        |
| right bottom  | 右 下                                                        |
| center top    | 中 上                                                        |
| center center | 中 中                                                        |
| center bottom | 中 下                                                        |
| x% y%         | 第一个值是水平位置，第二个值是垂直位置，左上角是0% 0%，右下角是100% 100% 。如果只指定了一个值，其他值默认是50%。默认是0% 0% |
| xpos ypos     | 单位是像素                                                   |

```css
.box{
    width: 600px;
    height: 600px;
    background-color: #fcc;
    background-image: url("images/img1.jpg");
    background-repeat: no-repeat;
    background-position: center;
}

```

**实时效果反馈**

**1.下列哪个属性可以设置背景图片位置的调整：**

A background-position

B background-repeat

C background-attachment

D background-size

**2.下列关于`background-repeat`属性描述错误的是：**

A repeat-x只向水平方向平铺

B repeat-y只向垂直方向平铺

C no-repeat不平铺

D repeat默认不平铺

**答案**

1=>A 2=>D

##  VII、文本属性

![image-20211201105726503](https://www.itbaizhan.com/wiki/imgs/image-20211201105726503.png)

### text-align

指定元素文本的水平对齐方式

| 值     | 描述                 |
| ------ | -------------------- |
| left   | 文本居左排列，默认值 |
| right  | 把文本排列到右边     |
| center | 把文本排列到中间     |

```css
h1 {text-align:center}
h2 {text-align:left}
h3 {text-align:right}

```

### text-decoration

text-decoration 属性规定添加到文本的修饰，下划线、上划线、删除线等

| 值           | 描述       |
| ------------ | ---------- |
| underline    | 定义下划线 |
| overline     | 定义上划线 |
| line-through | 定义删除线 |

```css
h1 {text-decoration:overline} 
h2 {text-decoration:line-through} 
h3 {text-decoration:underline}

```

### text-transform

text-transform 属性控制文本的大小写

| 值         | 描述                 |
| ---------- | -------------------- |
| captialize | 定义每个单词开头大写 |
| uppercase  | 定义全部大写字母     |
| lowercase  | 定义全部小写字母     |

```css
h1 {text-transform:uppercase;}
h2 {text-transform:capitalize;}
p {text-transform:lowercase;}

```

### text-indent

text-indent 属性规定文本块中首行文本的缩进

```css
p{
    text-indent:50px;
}

```

> **温馨提示**
>
> 负值是允许的。如果值是负数，将第一行左缩进

**实时效果反馈**

**1.下列哪个属性可以设置文本首字母大写：**

A text-indent

B text-transform

C text-decoration

D text-align

**答案**

1=>B

##  VIII、表格属性

![image-20211201112010039](https://www.itbaizhan.com/wiki/imgs/image-20211201112010039.png)

使用 CSS 可以使 HTML 表格更美观

### 表格边框

指定CSS表格边框，使用border属性

```css
table, td { 
    border: 1px solid black; 
}

```

### 折叠边框

border-collapse 属性设置表格的边框是否被折叠成一个单一的边框或隔开

```css
table { border-collapse:collapse; }
table,td { border: 1px solid black; }

```

### 表格宽度和高度

width和height属性定义表格的宽度和高度

```css
table { width:100%; } 
td { height:50px; }

```

### 表格文字对齐

表格中的文本对齐和垂直对齐属性

text-align属性设置水平对齐方式，向左，右，或中心

```css
td { text-align:right; }

```

垂直对齐属性设置垂直对齐

```css
td { height:50px; vertical-align:bottom; }
```

### 表格填充

如果在表的内容中控制空格之间的边框，应使用td和th元素的填充属性

```css
td { padding:15px; }
```

### 表格颜色

下面的例子指定边框的颜色，和th元素的文本和背景颜色

```css
table, td, th { border:1px solid green; } 
td { background-color:green; color:white; }
```

**实时效果反馈**

**1.下列哪个属性可以设置表格边框折叠：**

A text-align

B border-collapse

C border

D padding

**答案**

1=>B

##  IX、关系选择器

![image-20211202112056642](https://www.itbaizhan.com/wiki/imgs/image-20211202112056642.png)

**关系选择器分类**

1. 后代选择器
2. 子代选择器
3. 相邻兄弟选择器
4. 通用兄弟选择器

### 后代选择器

**定义**

选择所有被E元素包含的F元素，中间用空格隔开

**语法**

```css
E K{}
```

```css
<ul>
     <li>宝马</li>
     <li>奔驰</li>
</ul>
 <ol>
     <li>奥迪</li>
</ol>

```

```css
ul li{
    color:green;
}
```



### 子代选择器

**定义**

选择所有作为E元素的直接子元素F，对更深一层的元素不起作用，用>表示

**语法**

```css
E>F{}
```

```css
<div> 
    <a href="#">子元素1</a>
    <p> <a href="#">孙元素</a> </p>
    <a href="#">子元素2</a>
</div>
```

```css
div>a{
    color:red
}
```

### 相邻兄弟选择器

**定义**

选择紧跟E元素后的F元素，用加号表示，选择相邻的第一个兄弟元素，只能向下选择

**语法**

```css
E+F{}
```

```css
<h1>h1元素</h1> 
<p>第一个元素</p> 
<p>第二个元素</p>
```

```css
h1+p{
    color:red;
}
```

### 通用兄弟选择器

**定义**

选择E元素之后的所有兄弟元素F，作用于多个元素，用~隔开，只能向下选择

**语法**

```css
E~F{}
```

```css
<h1>h1元素</h1>
<p>第一个元素</p>
<p>第二个元素</p>
```

```css
h1~p{
    color:red;
}
```

**实时效果反馈**

**1.下列代码属于哪种关系选择器：**

```css
ul li{
    color:green;
}
```

A 后代选择器

B 子代选择器

C 相邻兄弟选择器

D 通用兄弟选择器

**答案**

1=>A

##  X、CSS 盒子模型(Box Model)

![image-20211206155745782](https://www.itbaizhan.com/wiki/imgs/image-20211206155745782.png)

### 概念

所有HTML元素可以看作盒子，在CSS中，"box model"这一术语是用来设计和布局时使用

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：

外边距（margin），边框（border），内边距（padding），和实际内容（content）

![image-20211202151036771](https://www.itbaizhan.com/wiki/imgs/image-20211202151036771.png)

1. Margin(外边距) - 清除边框外的区域，外边距是透明的（两个值：第一个值上下，第二个值左右）
2. Border(边框) - 围绕在内边距和内容外的边框
3. Padding(内边距) - 清除内容周围的区域（两个值：第一个值上下，第二个值左右）
4. Content(内容) - 盒子的内容，显示文本和图像

如果把盒子模型看作是一个生活中的快递，那么内容部分等同于你买的实物，内边距等同于快递盒子中的泡沫，边框等同于快递盒子，外边距等同于两个快递盒子之间的距离

![image-20211206160129321](https://www.itbaizhan.com/wiki/imgs/image-20211206160129321.png)

```css
<div></div>
```

```css
div{
    width: 100px;
    height: 100px;
    padding: 10px;
    border: 2px solid red;
    margin: 10px;
    background: green;
}
```



**实时效果反馈**

**1.下列盒子模型元素描述正确的是：**

A 外边距（margin）,边框（border）,内边距（padding）,和实际内容（content）

B 外边距（margin）,边框（border）,大小（font-size）,和实际内容（content）

C 外边距（margin）,背景（background）,内边距（padding）,和实际内容（content）

D 颜色（color）,边框（border）,内边距（padding）,和实际内容（content）

**答案**

1=>A

##  XI、弹性盒模型（flex box）

![image-20211206164317638](https://www.itbaizhan.com/wiki/imgs/image-20211206164317638.png)

### **定义**

弹性盒子是 CSS3 的一种新的布局模式

CSS3 弹性盒是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式

引入弹性盒布局模型的目的是提供一种更加有效的方式来对一个容器中的子元素进行排列、对齐和分配空白空间

### CSS3弹性盒内容

弹性盒子由弹性容器(Flex container)和弹性子元素(Flex item)组成

弹性容器通过设置 `display`属性的值为 `flex`将其定义为弹性容器

弹性容器内包含了一个或多个弹性子元素

> **温馨提示**
>
> 弹性容器外及弹性子元素内是正常渲染的。弹性盒子只定义了弹性子元素如何在弹性容器内布局

```css
<div class="flex-container">
    <div class="flex-item">flex item 1</div>
    <div class="flex-item">flex item 2</div>
    <div class="flex-item">flex item 3</div> 
</div>
<style>
    .flex-container {
        display: flex;
        width: 400px;
        height: 250px;
        background-color: lightgrey;
    }
    .flex-item {
        background-color: cornflowerblue;
        width: 100px;
        height: 100px;
        margin: 10px;
    }
</style>

```

> **温馨提示**
>
> 默认弹性盒里内容横向摆放

### 父元素上的属性

#### **display 属性**

`display:flex;`开启弹性盒

`display:flex;`属性设置后子元素默认水平排列

#### **flex-direction属性**

**定义**

flex-direction 属性指定了弹性子元素在父容器中的位置

**语法**

```css
flex-direction: row | row-reverse | column | column-reverse
```

1. row：横向从左到右排列（左对齐），默认的排列方式
2. row-reverse：反转横向排列（右对齐，从后往前排，最后一项排在最前面
3. column：纵向排列
4. column-reverse：反转纵向排列，从后往前排，最后一项排在最上面

```css
.flex-container {
    display: flex;
    flex-direction: column;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```

#### justify-content 属性

**定义**

内容对齐（justify-content）属性应用在弹性容器上，把弹性项沿着弹性容器的主轴线（main axis）对齐

**语法**

```css
justify-content: flex-start | flex-end | center 
```

1. `flex-start` 弹性项目向行头紧挨着填充。这个是默认值。第一个弹性项的main-start外边距边线被放置在该行的main-start边线，而后续弹性项依次平齐摆放
2. `flex-end` 弹性项目向行尾紧挨着填充。第一个弹性项的main-end外边距边线被放置在该行的main-end边线，而后续弹性项依次平齐摆放
3. `center` 弹性项目居中紧挨着填充。（如果剩余的自由空间是负的，则弹性项目将在两个方向上同时溢出）

```css
.flex-container {
    display: flex;
    justify-content: center;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}
```

#### align-items 属性

**定义**

`align-items` 设置或检索弹性盒子元素在侧轴（纵轴）方向上的对齐方式

**语法**

```css
align-items: flex-start | flex-end | center 
```

1. `flex-start` 弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界
2. `flex-end` 弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界
3. `center` 弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）

### **子元素上的属性**

#### flex

`flex` 根据弹性盒子元素所设置的扩展因子作为比率来分配剩余空间

默认为0，即如果存在剩余空间，也不放大

如果只有一个子元素设置，那么按扩展因子转化的百分比对其分配剩余空间。0.1即10%，1即100%，超出按100%

```css
<div class="flex-container">
    <div class="flex-item1">flex item 1</div>
    <div class="flex-item2">flex item 2</div>
    <div class="flex-item3">flex item 3</div> 
</div>
<style>
    .flex-container {
        display: flex;
        width: 400px;
        height: 250px;
        background-color: gold;
    }
    .flex-item1 {
        height: 150px;
        background-color: red;
        flex: 1;
    }
    .flex-item2 {
        height: 150px;
        background-color: green;
        flex: 2;
    }
    .flex-item3 {
        height: 150px;
        background-color: blue;
        flex: 1;
    }
</style>
```

**实时效果反馈**

**1.在弹性盒子模型中，一个元素块上下左右居中如何实现：**

A `{justify-content:center;align-items:center;}`

B `{flex-direction:center;align-items:center;}`

C `{justify-content:center;display:center;}`

D `{justify-content:center;flex:center;}`

**答案**

1=>A

##  XII、文档流

![image-20211208113754145](https://www.itbaizhan.com/wiki/imgs/image-20211208113754145.png)

文档流是文档中可显示对象在排列时所占用的位置/空间

例如：块元素自上而下摆放，内联元素，从左到右摆放

标准流里面的限制非常多，导致很多页面效果无法实现

1. 高矮不齐，底边对齐
2. 空白折叠现象
   1. 无论多少个空格、换行、tab，都会折叠为一个空格
   2. 如果我们想让img标签之间没有空隙，必须紧密连接

### 文档流产生的问题

#### 高矮不齐，底边对齐

![image-20211207184015709](https://www.itbaizhan.com/wiki/imgs/image-20211207184015709.png)

```css
<span>我是文本内容</span>
<img src="1.jpg" alt="">
```

```css
img{
    width: 200px;
}
```

#### 空格折叠

![image-20211207184304293](https://www.itbaizhan.com/wiki/imgs/image-20211207184304293.png)

```css
<span>我是文本     内容</span>
<img src="1.jpg" alt="">
```

```css
img{
    width: 200px;
}
```

#### 元素无空隙

![image-20211207184158189](https://www.itbaizhan.com/wiki/imgs/image-20211207184158189.png)

```css
<span>我是文本内容</span>
<img src="1.jpg" alt=""><img src="1.jpg" alt="">
```

```css
img{
    width: 200px;
}
```

如果我们现在就要并排顶部对齐，那该怎么办呢？办法是：移民！脱离标准流！

### 脱离文档流

使⼀个元素脱离标准文档流有三种方式

1. 浮动
2. 绝对定位
3. 固定定位

**实时效果反馈**

**1.下列哪种方式不能脱离文档流：**

A 浮动

B 绝对定位

C 固定定位

D 相对布局

**答案**

1=>D

##  XIII、浮动

![image-20211208114221274](https://www.itbaizhan.com/wiki/imgs/image-20211208114221274.png)

### 浮动的定义

`float`属性定义元素在哪个方向浮动，任何元素都可以浮动。

| 值    | 描述         |
| ----- | ------------ |
| left  | 元素向左浮动 |
| right | 元素向右浮动 |

### 浮动的原理

1. 浮动以后使元素脱离了文档流
2. 浮动只有左右浮动，没有上下浮动

### 元素向左浮动

脱离文档流之后，元素相当于在页面上面增加一个浮层来放置内容。此时可以理解为有两层页面，一层是底层的原页面，一层是脱离文档流的上层页面，所以会出现折叠现象

![image-20211207190501956](https://www.itbaizhan.com/wiki/imgs/image-20211207190501956.png)

```css
<div class="box"></div>
<div class="container"></div>
```

```css
.container{
    width: 200px;
    height: 200px;
    background-color: #81c784;
}


.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
}
```

### 元素向右浮动

![image-20211207190746861](https://www.itbaizhan.com/wiki/imgs/image-20211207190746861.png)

```css
<div class="box"></div>
<div class="container"></div>
```

```css
.container{
    width: 200px;
    height: 200px;
    background-color: #81c784;
}
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: right;
}
```



### 所有元素向左浮动

当所有元素同时浮动的时候，会变成水平摆放，向左或者向右

![image-20211207191044382](https://www.itbaizhan.com/wiki/imgs/image-20211207191044382.png)

```css
<div class="box"></div>
<div class="box"></div>
<div class="box"></div>
```

```css
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 0 5px;
}
```



### 当容器不足时

当容器不足以横向摆放内容时候，会在下一行摆放

![image-20211207191358743](https://www.itbaizhan.com/wiki/imgs/image-20211207191358743.png)

```css
<div class="container">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
</div>
```

```css
.container{
    width: 250px;
    height: 300px;
    border: 1px solid red;
}
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 5px;
}
```

**实时效果反馈**

**1.下列关于浮动描述错误的是：**

A 浮动以后使元素脱离了文档流

B 浮动只有左右浮动，没有上下浮动

C `float`属性定义元素在哪个方向浮动，任何元素都可以浮动

D 当容器不足以横向摆放内容时候，会隐藏元素

**答案**

1=>D

## XIV、清除浮动

![image-20211208114757773](https://www.itbaizhan.com/wiki/imgs/image-20211208114757773.png)

### 浮动副作用

当元素设置float浮动后，该元素就会脱离文档流并向左/向右浮动，

1. 浮动元素会造成父元素高度塌陷
2. 后续元素会受到影响

![image-20211207191734044](https://www.itbaizhan.com/wiki/imgs/image-20211207191734044.png)

```css
<div class="container">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
</div>
```

```css
.container{
    border: 1px solid red;
}
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 5px;
}

```

![image-20211207192553249](https://www.itbaizhan.com/wiki/imgs/image-20211207192553249.png)

```css
<div class="box"></div>
<div class="box"></div>
<div class="box"></div>
<div class="nav"></div>

```

```css
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 5px;
}
.nav{
    width: 100px;
    height: 100px;
    background-color: red;
}

```



### 清除浮动

当父元素出现塌陷的时候，对布局是不利的，所以我们必须清除副作用

解决方案有很多种

1. 父元素设置高度
2. 受影响的元素增加clear属性
3. overflow清除浮动
4. 伪对象方式

#### 父元素设置高度

如果父元素高度塌陷，可以给父元素设置高度，撑开元素本身大小

![image-20211207192110432](https://www.itbaizhan.com/wiki/imgs/image-20211207192110432.png)

```css
<div class="container">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
</div>

```

```css
.container{
    height: 300px;
    width: 350px;
    border: 1px solid red;
}
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 5px;
}

```



#### overflow清除浮动

如果有父级塌陷，并且同级元素也收到了影响，可以使用`overflow`清除浮动

这种情况下，父布局不能设置高度

父级标签的样式里面加: `overflow:hidden;clear: both;`

![image-20211207193235102](https://www.itbaizhan.com/wiki/imgs/image-20211207193235102.png)

```css
<div class="container">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
</div>
<div class="nav"></div>

```

```css
.container{
    width: 350px;
    border: 1px solid red;
    overflow: hidden;
    clear: both;
}
.box{
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 5px;
}
.nav{
    width: 100px;
    height: 100px;
    background-color: red;
}

```



#### 伪对象方式

如果有父级塌陷，并且同级元素也收到了影响，还可以使用伪对象方式处理

为父标签添加伪类`after`,设置空的内容，并且使用`clear:both`;

这种情况下，父布局不能设置高度

![image-20211207193547613](https://www.itbaizhan.com/wiki/imgs/image-20211207193547613.png)

```css
<div class="container">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
</div>
<div class="nav"></div>

```

```css
.container {
    width: 350px;
    border: 1px solid red;
}
.container::after {
    content: "";
    display: block;
    clear: both;
}
.box {
    width: 100px;
    height: 100px;
    background-color: #fff176;
    float: left;
    margin: 5px;
}
.nav {
    width: 100px;
    height: 100px;
    background-color: red;
}

```

**实时效果反馈**

**1.下列关于清除浮动的方法，描述错误的是：**

A 如果父元素塌陷，可以设置父元素高度消除浮动的副作用

B 如果后续元素受到浮动影响，可以使用`clear: both;`清除

C 如果父元素塌陷，可以使用伪对象方式清除

D 如果父元素塌陷同时影响后续元素，可以使用`float`清除

**答案**

1=>D

##  XV、定位

![image-20211208115836062](https://www.itbaizhan.com/wiki/imgs/image-20211208115836062.png)

### 定义

`position`属性指定了元素的定位类型

| 值       | 描述     |
| -------- | -------- |
| relative | 相对定位 |
| absolute | 绝对定位 |
| fixed    | 固定定位 |

其中，绝对定位和固定定位会脱离文档流

设置定位之后：可以使用四个方向值进行调整位置：`left、top、right、bottom`

### 相对定位

```css
<div class="box"></div>
```

```css
.box{
    width: 200px;
    height: 200px;
    background-color: red;
    position: relative;
    left: 100px;
}
```



### 绝对定位

```css
<div class="box1"></div>
<div class="box2"></div>

```

```css
.box1{
    width: 200px;
    height: 200px;
    background-color: red;
    position:absolute;
    left: 50px;
}
.box2{
    width: 300px;
    height: 300px;
    background-color: green;
}

```



### 固定定位

```css
<div class="box1"></div>
<div class="box2"></div>
.box1{
    width: 200px;
    height: 200px;
    background-color: red;
    position:fixed;
    left: 50px;
}
.box2{
    width: 300px;
    height: 300px;
    background-color: green;
}

```

> **温馨提示**
>
> 设置定位之后，相对定位和绝对定位他是相对于具有定位的父级元素进行位置调整，如果父级元素不存在定位，则继续向上逐级寻找，直到顶层文档

```css
<div class="container">
    <div class="box"></div>
</div>

```

```css
.container{
    width: 300px;
    height: 300px;
    background-color: #666;
    position: relative;
    left: 200px;
}
.box{
    width: 200px;
    height: 200px;
    background-color: red;
    position:absolute;
}

```



### Z-index

`z-index`属性设置元素的堆叠顺序。拥有更高堆叠顺序的元素总是会处于堆叠顺序较低的元素的前面

```css
<div class="box1"></div>
<div class="box2"></div>

```

```css
.box1{
    width: 200px;
    height: 200px;
    background-color: red;
    position:absolute;
    z-index: 2;
}
.box2{
    width: 300px;
    height: 300px;
    background-color: green;
    position:absolute;
    z-index: 1;
}

```

**实时效果反馈**

**1.下列哪种属性设置不会脱离文档流：**

A 相对定位

B 绝对定位

C 固定定位

D 浮动

**答案**

1=>A

## XVI、CSS3新特性

![image-20220428000457846](https://www.itbaizhan.com/wiki/imgs/image-20220428000457846.png)

### 圆角

使用 CSS3 `border-radius` 属性，你可以给任何元素制作 "圆角"

`border-radius` 属性，可以使用以下规则：

1. 四个值: 第一个值为左上角，第二个值为右上角，第三个值为右下角，第四个值为左下角
2. 三个值: 第一个值为左上角, 第二个值为右上角和左下角，第三个值为右下角
3. 两个值: 第一个值为左上角与右下角，第二个值为右上角与左下角
4. 一个值： 四个圆角值相同

```css
<div class="box1"></div>
<div class="box2"></div>
<div class="box3"></div>
```

```css
div{
    margin: 10px;
}
.box1 {
    border-radius: 15px 50px 30px 5px;
    background: #8AC007;
    padding: 20px;
    width: 200px;
    height: 150px;
}
.box2 {
    border-radius: 15px 50px 30px;
    background: #8AC007;
    padding: 20px;
    width: 200px;
    height: 150px;
}
.box3 {
    border-radius: 15px 50px;
    background: #8AC007;
    padding: 20px;
    width: 200px;
    height: 150px;
}
```

### 阴影

box-shadow 向框添加一个或多个阴影。

```css
box-shadow: h-shadow v-shadow blur color;
```

| 值       | 描述                 |
| -------- | -------------------- |
| h-shadow | 必选，水平阴影的位置 |
| v-shadow | 必选，垂直阴影的位置 |
| blur     | 可选，模糊距离       |
| color    | 可选，阴影的颜色     |

![image-20211209100532071](https://www.itbaizhan.com/wiki/imgs/image-20211209100532071.png)

```css
<div class="box"></div>
```

```css
.box {
    width: 200px;
    height: 200px;
    background-color: #8ac007;
    margin: 50px;
    box-shadow: 10px 10px green;
}
```

给阴影添加一个模糊效果

![image-20211209100710034](https://www.itbaizhan.com/wiki/imgs/image-20211209100710034.png)

```css
.box {
    width: 200px;
    height: 200px;
    background-color: #8ac007;
    margin: 50px;
    box-shadow: 10px 10px 5px green;
}

```

三个方向的阴影效果

![image-20211209100828270](https://www.itbaizhan.com/wiki/imgs/image-20211209100828270.png)

```css
.box {
    width: 200px;
    height: 200px;
    background-color: #8ac007;
    margin: 50px;
    box-shadow: 0 10px 30px rgba(0,0,0,.5);
}

```

**实时效果反馈**

**1.将一个正方形盒子改成圆形，下列哪个设置可以实现：**

A `{border:50%;}`

B `{border-radius:50%;}`

C `{border-radius:50px;}`

D `{border:50px;}`

**2.完成一个水平垂直阴影位置为0，模糊度为10px，颜色为黑色半透明：**

A `box-shadow: 0px 0px 10px rgba(0,0,0,0.5);`

B `box-shadow: 0px 0px rgba(0,0,0,0.5);`

C `box-shadow: 0px 10px 10px #000;`

D `box-shadow: 10px 10px 0px rgba(0,0,0,0.5);`

**答案**

1=>B 2=>A

##  XVII、动画

![image-20211209150150127?v=1.0.0](https://www.itbaizhan.com/wiki/imgs/image-20211209150150127.png?v=1.0.0)

动画是使元素从一种样式逐渐变化为另一种样式的效果

您可以改变任意多的样式任意多的次数

请用百分比来规定变化发生的时间，或用关键词 "from" 和 "to"，等同于 0% 和 100%

0% 是动画的开始，100% 是动画的完成。

### @keyframes创建动画

使用`@keyframes`规则，你可以创建动画

```css
@keyframes name {
    from|0%{
        css样式
    }
    percent{
        css样式
    }
    to|100%{
        css样式
    }
}

```

name：动画名称，开发人员自己命名；

percent：为百分比值，可以添加多个百分比值；

### animation执行动画

```css
animation: name duration timing-function delay iteration-count direction;
```

| 值                   | 描述                                                      |
| -------------------- | --------------------------------------------------------- |
| name                 | 设置动画的名称                                            |
| duration             | 设置动画的持续时间                                        |
| timing-function      | 设置动画效果的速率（如下）                                |
| delay                | 设置动画的开始时间（延时执行）                            |
| iteration-count      | 设置动画循环的次数，infinite为无限次数的循环              |
| direction            | 设置动画播放的方向（如下）                                |
| animation-play-state | 控制动画的播放状态：running代表播放，而paused代表停止播放 |

| timing-function值 | 描述             |
| ----------------- | ---------------- |
| ease              | 逐渐变慢（默认） |
| linear            | 匀速             |
| ease-in           | 加速             |
| ease-out          | 减速             |
| ease-in-out       | 先加速后减速     |

| direction值 | 描述                                             |
| ----------- | ------------------------------------------------ |
| normal      | 默认值为normal表示向前播放                       |
| alternate   | 动画播放在第偶数次向前播放，第奇数次向反方向播放 |

**切换背景颜色**

```css
<div class="animation"></div>
```

```css
.animation {
    width: 300px;
    height: 300px;
    background-color: red;
    animation: anima 5s linear 5s infinite;
}
.animation:hover {
    animation-play-state: paused;
}
@keyframes anima {
    0% {
        background-color: red;
    }
    50% {
        background-color: green;
    }
    100% {
        background-color: blueviolet;
    }
}

```

**呼吸效果**

```css
<div class="box"></div>
```

```css
.box {
    width: 500px;
    height: 400px;
    margin: 40px auto;
    background-color: #2b92d4;
    border-radius: 5px;
    box-shadow: 0 1px 2px rgba(0, 0, 0, .3);
    animation: breathe 2700ms ease-in-out infinite alternate;
}
@keyframes breathe {
    0% {
        opacity: .2;
        box-shadow: 0 1px 2px rgba(255, 255, 255, 0.1)
    }
    50% {
        opacity: .5;
        box-shadow: 0 1px 2px rgba(18, 190, 84, 0.76)
    }
    100% {
        opacity: 1;
        box-shadow: 0 1px 30px rgba(59, 255, 255, 1)
    }
}

```

**实时效果反馈**

**1.动画属性中，`iteration-count: infinite`属性的作用是：**

A 设置动画效果时间

B 设置动画效果速率

C 设置动画的开始时间

D 设置动画无限循环

**答案**

1=>D

##  XVIII、媒体查询

![image-20211210145646235](https://www.itbaizhan.com/wiki/imgs/image-20211210145646235.png)

媒体查询能使页面在不同在终端设备下达到不同的效果

媒体查询会根据设备的大小自动识别加载不同的样式

### 设置meta标签

使用设备的宽度作为视图宽度并禁止初始的缩放。在标签里加入这个meta标签。 `<head>`

```css
<meta name="viewport" content="width=device-width, initial-scale=1,maximum-scale=1, user-scalable=no">
```

**参数解释**

1. `width = device-width` 宽度等于当前设备的宽度
2. `initial-scale` 初始的缩放比例（默认设置为1.0）
3. `maximum-scale` 允许用户缩放到的最大比例（默认设置为1.0）
4. `user-scalable` 用户是否可以手动缩放（默认设置为no）

### 媒体查询语法

```css
@media screen and (max-width: 768px) {
    /* 设备小于768px加载样式 */
    body{
        background-color: red;
    }
}
@media screen and (max-width: 992px) and (min-width: 768px) {
     /* 设备小于768px但小于992px加载样式  */
     body{
        background-color: pink;
     }
}
@media screen and (min-width: 992px) {
    /* 设备大于992px加载样式 */
    body{
        background-color: green;
    }
}

```

**实时效果反馈**

**1.下列代码媒体查询，运行在屏幕宽度为800px的设备上，背景颜色是：**

```css
@media screen and (max-width: 768px) {
    body{
        background-color: red;
    }
}
@media screen and (max-width: 992px) and (min-width: 768px) {
     body{
        background-color: pink;
     }
}
@media screen and (min-width: 992px) {
    body{
        background-color: green;
    }
}

```

A red(红色)

B pink(粉色)

C green(绿色)

D black(黑色)

**答案**

1=>B

##  XIX、雪碧图

![1](https://www.itbaizhan.com/wiki/imgs/1.png)

CSS Sprite也叫CSS精灵图、CSS雪碧图，是一种网页图片应用处理方式。它允许你将一个页面涉及到的所有零星图片都包含到一张大图中去

### 优点

1. 减少图片的字节
2. 减少网页的http请求，从而大大的提高页面的性能

### 原理

1. 通过background-image引入背景图片
2. 通过background-position把背景图片移动到自己需要的位置

### 实例

```css
<i class="icon1"></i>
<i class="icon2"></i> 
```

```css
.icon1 {
    display: block;
    background-image: url(1.png);
    background-position: -20px 0;
    width: 45px;
    height: 70px;
}
.icon2 {
    display: block;
    background-image: url(1.png);
    background-position: -93px -84px;
    width: 45px;
    height: 70px;
}
```

## XX、字体图标

![image-20211210151709114?v=1.0.1](https://www.itbaizhan.com/wiki/imgs/image-20211210151709114.png?v=1.0.1)

我们会经常用到一些图标。但是我们在使用这些图标时，往往会遇到失真的情况，而且图片数量很多的话，页面加载就越慢。所以，我们可以使用字体图标的方式来显示图标，既解决了失真的问题，也解决了图片占用资源的问题

常用字体图标库：[阿里字体图标库](https://iconfont.cn/)

### 优点

1. 轻量性：加载速度快，减少http请求
2. 灵活性：可以利用CSS设置大小颜色等
3. 兼容性：网页字体支持所有现代浏览器，包括IE低版本

### 使用字体图标

1. 注册账号并登录
2. 选取图标或搜索图标
3. 添加购物车
4. 下载代码
5. 选择`font-class`引用

```css
<span class="iconfont icon-add-circle"></span>
```

```css
<link rel="stylesheet" href="./css/iconfont.css">
.iconfont{
    font-size: 35px;
    color: red;
}
```

# 四、JavaScript简介

![image-20220510204512962](https://www.itbaizhan.com/wiki/imgs/image-20220510204512962.png)

## I、JavaScript介绍

JavaScript 是一种轻量级的脚本语言。所谓“脚本语言”，指的是它不具备开发操作系统的能力，而是只用来编写控制其他大型应用程序的“脚本”。

JavaScript 是一种嵌入式（embedded）语言。它本身提供的核心语法不算很多

### 为什么学习 JavaScript

- 操控浏览器的能力
- 广泛的使用领域
- 易学性

### JavaScript与ECMAScript的关系

ECMAScript和JavaScript的关系是，前者是后者的规格，后者是前者的一种实现。在日常场合，这两个词是可以互换的。

### JavaScript版本

![img](https://www.itbaizhan.com/wiki/imgs/SNAGHTML4acb84a.PNG)

**实时效果反馈**

**1. ECMAScript和JavaScript关系：**

A JavaScript是ECMAScript的父级

B JavaScript是ECMAScript的子级

C 不存在ECMAScript这个名字

D 前者是后者的规格，后者是前者的一种实现

**2. 以下哪个不是JavaScript的优点:**

A JavaScript操控浏览器的能力

B JavaScript广泛的使用领域

C JavaScript易学性

D JavaScript可以实现操作系统

**答案**

1=>D 2=>D

##  II、JavaScript语句、标识符

![image-20211111170905937](https://www.itbaizhan.com/wiki/imgs/image-20211111170905937.png)

### 语句

JavaScript 程序的单位是行（line），也就是一行一行地执行。一般情况下，每一行就是一个语句

```javascript
var num = 10;
```

语句以分号结尾，一个分号就表示一个语句结束

### 标识符

标识符（identifier）指的是用来识别各种值的合法名称。最常见的标识符就是变量名

标识符是由：字母、美元符号($)、下划线(_)和数字组成，其中数字不能开头

> **温馨提示**
>
> 中文是合法的标识符，可以用作变量名（不推荐）

### JavaScript保留关键字

以下关键字不需要强行记忆！

> JavaScript有一些保留字，不能用作标识符：arguments、break、case、catch、class、const、continue、debugger、default、delete、do、else、enum、eval、export、extends、false、finally、for、function、if、implements、import、in、instanceof、interface、let、new、null、package、private、protected、public、return、static、super、switch、this、throw、true、try、typeof、var、void、while、with、yield。

**实时效果反馈**

**1. 以下哪个命名是正确的：**

A `var const = 10;`

B `var 10Num = 20;`

C `var @A = 30;`

D `var age=20;`

**2. 以下哪个是标识符命名规则:**

A 字母、美元符号($)、下划线(_)和数字

B 字母、美元符号($)、下划线(_)和数字，其中数字不能开头

C 字母、美元符号($)、百分号(%)和数字，其中数字不能开头

D 字母、美元符号($)、下划线(_)和特殊符号

**答案**

1=>D 2=>B

##  III、变量

![image-20211111162356047](https://www.itbaizhan.com/wiki/imgs/image-20211111162356047.png)

```javascript
var num = 10; 
```

#### 变量的重新赋值

```javascript
var num = 10;
num = 20;
```

### 变量提升

JavaScript 引擎的工作方式是，先解析代码，获取所有被声明的变量，然后再一行一行地运行。这造成的结果，就是所有的变量的声明语句，都会被提升到代码的头部，这就叫做变量提升（hoisting）。

```javascript
console.log(num);
var num = 10; // 结果是什么呢？
```

**实时效果反馈**

**1. 以下代码打印正确的是：**

```javascript
console.log(num);
var num = 10; 
```

A 10

B 错误

C undefined

D num

**答案**

1=>C

##  IV、JavaScript引入到文件

![image-20211018115501776](https://www.itbaizhan.com/wiki/imgs/image-20211018115501776.png)

### 嵌入到HTML文件中

```javascript
<body>
    <script>
        var age = 20
    </script>
</body>

```



### 引入本地独立JS文件

```javascript
<body>
    <script type="text/javascript" src="./itbaizhan.js">        </script>
</body>

```

### 引入网络来源文件

```javascript
<body>
    <script src="https://cdn.bootcdn.net/ajax/libs/jquery/3.6.0/jquery.min.js"> </script>
</body>
```

**实时效果反馈**

**1. 以下哪种不是JS文件引入到HTML文件中的方式：**

A JS嵌入到HTML文件中

B 引入本地独立JS文件

C 引入网络来源的JS文件

D JS嵌入到CSS文件中

**2. 以下代码是哪种JS引入到HTML文件中的方式:**

```javascript
<body>
    <script type="text/javascript" src="./itbaizhan.js">        </script>
</body>
```

A JS嵌入到HTML文件中

B 引入本地独立JS文件

C 引入网络来源的JS文件

D JS嵌入到CSS文件中

**答案**

1=>D 2=>B

##  V、JavaScript注释与常见输出方式

![image-20211018144940611](https://www.itbaizhan.com/wiki/imgs/image-20211018144940611.png)

### JavaScript注释

源码中注释是不被引擎所解释的，它的作用是对代码进行解释。Javascript 提供两种注释的写法：一种是单行注释，用//起头；另一种是多行注释，放在/*和*/之间。

```javascript
// 这是单行注释


/*
 这是
 多行
 注释
*/

```

嵌入在HTML文件中的注释

```javascript
<!-- 注释 -->
```

> **温馨提示**
>
> 注释的快捷键：`ctrl + /`

### JavaScript输出方式

JavaScript有很多种输出方式，都可以让我们更直观的看到程序运行的结果

```javascript
// 在浏览器中弹出一个对话框,然后把要输出的内容展示出来,alert都是把要输出的内容首先转换为字符串然后在输出的
alert("要输出的内容");


document.write("要输出的内容"); 


// 在控制台输出内容
console.log("要输出的内容");

```

**实时效果反馈**

**1. 下述代码横线处应填写的代码：**

```javascript
document.___("要输出的内容"); 
```

A document

B alert

C log

D write

**2. 下述代码横线处应填写的代码:**

```javascript
console.___("要输出的内容");
```

A document

B alert

C log

D write

**答案**

1=>D 2=>C

## VI、数据类型

![image-20211018132222139](https://www.itbaizhan.com/wiki/imgs/image-20211018132222139.png)

### 数据类型分类

JavaScript 语言的每一个值，都属于某一种数据类型。JavaScript 的数据类型，共有六种。（ES6 又新增了第七种 Symbol 类型的值和第八种 BigInt类型，当前课程暂不涉及）

### 数据类型分类

#### 原始类型(基础类型)

![image-20211018132723076?v=1.0.0](https://www.itbaizhan.com/wiki/imgs/image-20211018132723076.png?v=1.0.0)

```javascript
var age = 20;
var name = "尚学堂";
var learn = true;

```

#### 合成类型(复合类型)

对象：因为一个对象往往是多个原始类型的值的合成，可以看作是一个存放各种值的容器

![image-20211018132851693?v=1.0.0](https://www.itbaizhan.com/wiki/imgs/image-20211018132851693.png?v=1.0.0)

```javascript
var user = {
    name:"尚学堂",
    age:20,
    learn:true
}

```

> **温馨提示**
>
> 至于undefined和null，一般将它们看成两个特殊值。

**实时效果反馈**

**1. 以下那个是字符串类型数据：**

A `var age = 20;`

B `var name = "尚学堂"`

C `var learn = true`

D `var user = {}`

**2. 以下关于原始数据类型分类正确的是:**

A 数值、字符串、布尔值、对象

B 数值、字符串、布尔值、null

C 数值、字符串、布尔值、undefined

D 数值、字符串、布尔值

**答案**

1=>B 2=>D

##  VII、typeof运算符

![image-20211018134825571](https://www.itbaizhan.com/wiki/imgs/image-20211018134825571.png)

JavaScript 有三种方法，可以确定一个值到底是什么类型。而我们现在需要接触到的就是typeof

### 数值返回number

```javascript
typeof 123 // "number"
```

### 字符串返回string

```javascript
typeof '123' // "string"
```

### 布尔值返回boolean

```javascript
typeof false // "boolean"
```

### 对象返回object

```javascript
typeof {} // "object"
```

### unll和undefined的区别

null与undefined都可以表示“没有”，含义非常相似。将一个变量赋值为undefined或null，老实说，语法效果几乎没区别。既然含义与用法都差不多，为什么要同时设置两个这样的值，这不是无端增加复杂度，令初学者困扰吗？这与历史原因有关

**实时效果反馈**

**1. 下列字符串数据类型的关键字是：**

A number

B string

C boolean

D object

**2. 以下代码执行结果正确的是:**

```javascript
console.log(typeof 100)
```

A number

B string

C boolean

D object

**答案**

1=>B 2=>A

##  VIII、for循环语句实操

![image-20220512154359129](https://www.itbaizhan.com/wiki/imgs/image-20220512154359129.png)

### 循环输出1~100之间数字的和

```javascript
var sum=0;
for(var i=1;i<=100;i++){
    sum+=i;
}
console.log(sum);

```

### 循环输出1000以内的奇数

```javascript
for(i = 0 ; i<1000; i ++){
    if( i % 2 ==1){
        console.log( i + " ");   
    }
}

```

### 打印九九乘法表

![image-20211020172520296](https://www.itbaizhan.com/wiki/imgs/image-20211020172520296.png)

```javascript
for(var i = 1;i <= 9;i++){
    document.write("<br>"); 
    for(var j = 1;j <= i;j++){
        sum = i * j;
        document.write(i ,"*",j ,"=",sum," ");
    }
}

```

##  IX、字符串

![image-20220512165508422](https://www.itbaizhan.com/wiki/imgs/image-20220512165508422.png)

字符串就是零个或多个排在一起的字符，放在单引号或双引号之中

```javascript
'itbaizhan'
"itbaizhan"
```

单引号字符串的内部，可以使用双引号。双引号字符串的内部，可以使用单引号

```javascript
'key = "value"'
"It's a long itbaizhan"
```

如果要在单引号字符串的内部，使用单引号，就必须在内部的单引号前面加上反斜杠，用来转义。双引号字符串内部使用双引号，也是如此

```javascript
'Did she say \'Hello\'?'
// "Did she say 'Hello'?"


"Did she say \"Hello\"?"
// "Did she say "Hello"?"

```

> **温馨提示**
>
> 字符串默认只能写在一行内，分成多行将会报错

如果长字符串必须分成多行，可以在每一行的尾部使用反斜杠

```javascript
var longString = 'Long \
long \
string';
longString
// "Long long long string"

```

### length 属性

length属性返回字符串的长度，该属性也是无法改变的

```javascript
var s = 'itbaizhan';
s.length // 9

```

**实时效果反馈**

**1. 下列字符串，横线处应该填写的代码是：**

```javascript
"Did she say ___"Hello___"?"
```

A "" ''

B '' ""

C \ \

D "" ""

**答案**

1=>C

## X、字符串方法 

### 1、字符串方法_charAt()

![image-20220512164512910](https://www.itbaizhan.com/wiki/imgs/image-20220512164512910.png)

`charAt`方法返回指定位置的字符，参数是从`0`开始编号的

```javascript
var s = new String('itbaizhan');


s.charAt(1) // "t"
s.charAt(s.length - 1) // "n"

```

如果参数为负数，或大于等于字符串的长度，`charAt`返回空字符串

```javascript
'itbaizhan'.charAt(-1) // ""
'itbaizhan'.charAt(9) // ""

```

**实时效果反馈**

**1. 下列字符串方法charAt的应用，代码输出结果是：**

```javascript
'itbaizhan'.charAt(9);
```

A o

B 0

C hello

D ""

**答案**

1=>D

###  2、字符串方法_concat()

![image-20220512164646652](https://www.itbaizhan.com/wiki/imgs/image-20220512164646652.png)

`concat`方法用于连接两个字符串，返回一个新字符串，不改变原字符串

```javascript
var s1 = 'itbaizhan';
var s2 = 'sxt';


s1.concat(s2) // "itbaizhansxt"
s1 // "itbaizhan"

```

该方法可以接受多个参数

```javascript
'sxt'.concat('itbaizhan', 'bjsxt') // "sxtitbaizhanbjsxt"
```

如果参数不是字符串，`concat`方法会将其先转为字符串，然后再连接

```javascript
var one = 1;
var two = 2;
var three = '3';


''.concat(one, two, three) // "123"

```

**实时效果反馈**

**1. 下列字符串方法concat的应用，代码输出结果是：**

```javascript
var one = 1;
var two = 2;
var three = '3';


console.log(''.concat(one, two, three) )
console.log(one + two + three )

```

A 123 33

B 123 123

C 33 33

D 6 6

**答案**

1=>A

###  3、字符串方法_substring()

![image-20220512164812314](https://www.itbaizhan.com/wiki/imgs/image-20220512164812314.png)

`substring`方法用于从原字符串取出子字符串并返回，不改变原字符串。它的第一个参数表示子字符串的开始位置，第二个位置表示结束位置（返回结果不含该位置）

```javascript
'itbaizhan'.substring(0, 2) // "it"
```

如果省略第二个参数，则表示子字符串一直到原字符串的结束

```javascript
'itbaizhan'.substring(2) // "baizhan"
```

如果第一个参数大于第二个参数，`substring`方法会自动更换两个参数的位置

```javascript
'itbaizhan'.substring(9, 2) // "baizhan"
// 等同于
'itbaizhan'.substring(2, 9) // "baizhan"

```

如果参数是负数，`substring`方法会自动将负数转为0

```javascript
'itbaizhan'.substring(-3) // "itbaizhan"
'itbaizhan'.substring(2, -3) // "it"

```

**实时效果反馈**

**1. 下列字符串方法substring的应用，代码输出结果是：**

```javascript
 'itbaizhan'.substring(5, -3)
```

A ""

B itbaizhan

C itbai

D bai

**答案**

1=>C

###  4、字符串方法_substr()

![image-20220512164914465](https://www.itbaizhan.com/wiki/imgs/image-20220512164914465.png)

`substr`方法用于从原字符串取出子字符串并返回，不改变原字符串，跟`substring`方法的作用相同

`substr`方法的第一个参数是子字符串的开始位置（从0开始计算），第二个参数是子字符串的长度

```javascript
 'itbaizhan'.substr(2, 7); // baizhan
```

如果省略第二个参数，则表示子字符串一直到原字符串的结束

```javascript
 'itbaizhan'.substr(2) // "baizhan"
```

如果第一个参数是负数，表示倒数计算的字符位置。如果第二个参数是负数，将被自动转为0，因此会返回空字符串

```javascript
'itbaizhan'.substr(-7) // "baizhan"
'itbaizhan'.substr(4, -1) // ""

```

**实时效果反馈**

**1. 下列字符串方法substr的应用，代码输出结果是：**

```javascript
 'itbaizhan'.substr(2, -2)
```

A ""

B itbaizhan

C itbai

D bai

**答案**

1=>A

###  5、字符串方法_indexOf()

![image-20220512165035598](https://www.itbaizhan.com/wiki/imgs/image-20220512165035598.png)

`indexOf`方法用于确定一个字符串在另一个字符串中第一次出现的位置，返回结果是匹配开始的位置。如果返回`-1`，就表示不匹配

```javascript
'hello world'.indexOf('o') // 4
'itbaizhan'.indexOf('sxt') // -1

```

`indexOf`方法还可以接受第二个参数，表示从该位置开始向后匹配

```javascript
 'hello world'.indexOf('o', 6) // 7
```

**实时效果反馈**

**1. 下列字符串方法indexOf的应用，代码输出结果是：**

```javascript
 'itbaizhan'.indexOf("z",6)
```

A -1

B itbaizhan

C 0

D 5

**答案**

1=>A

###  6、字符串方法_trim()

![image-20220512165141908](https://www.itbaizhan.com/wiki/imgs/image-20220512165141908.png)

`trim`方法用于去除字符串两端的空格，返回一个新字符串，不改变原字符串

```javascript
'  hello world  '.trim()
// "hello world"

```

该方法去除的不仅是空格，还包括制表符（`\t`、`\v`）、换行符（`\n`）和回车符（`\r`）

```javascript
'\r\nitbaizhan \t'.trim() // 'itbaizhan'
```

ES6扩展方法，`trimEnd()`和`trimStart()`方法

```javascript
"   itbaizhan   ".trimEnd(); //    itbaizhan
"   itbaizhan   ".trimStart(); // itbaizhan   
```

**实时效果反馈**

**1. 下列字符串方法trim的应用，代码输出结果是：**

```javascript
'\r\n itbaizhan \t  '.trim()
```

A \r\n itbaizhan \t

B \r\nitbaizhan\t

C \r\nitbaizhan \t

D itbaizhan

**答案**

1=>D

###  7、字符串方法_split()

![image-20220512165305087](https://www.itbaizhan.com/wiki/imgs/image-20220512165305087.png)

`split`方法按照给定规则分割字符串，返回一个由分割出来的子字符串组成的数组

```javascript
'it|sxt|baizhan'.split('|') // ["it", "sxt", "baizhan"]
```

如果分割规则为空字符串，则返回数组的成员是原字符串的每一个字符。

```javascript
'a|b|c'.split('') // ["a", "|",  "b","|", "c"]
```

如果省略参数，则返回数组的唯一成员就是原字符串

```javascript
 'it|sxt|bz'.split() // [it|sxt|bz]
```

`split`方法还可以接受第二个参数，限定返回数组的最大成员数。

```javascript
'it|sxt|bz'.split('|', 0) // []
'it|sxt|bz'.split('|', 1) // ["it"]
'it|sxt|bz'.split('|', 2) // ["it", "sxt"]
'it|sxt|bz'.split('|', 3) // ["it", "sxt", "bz"]
'it|sxt|bz'.split('|', 4) // ["it", "sxt", "bz"]

```

**实时效果反馈**

**1. 下列字符串操作代码，执行结果是：**

```javascript
"itbaizhan".split("");
```

A `[itbaizhan]`

B `['it','haizhan']`

C `['i', 't', 'b', 'a', 'i', 'z', 'h', 'a', 'n']`

D `'i', 't', 'b', 'a', 'i', 'z', 'h', 'a', 'n'`

**答案**

1=>C

##  XI、数组

![image-20211022115344470](https://www.itbaizhan.com/wiki/imgs/image-20211022115344470.png)

数组（array）是按次序排列的一组值。每个值的位置都有编号（从0开始），整个数组用方括号表示。

```javascript
var arr = ['sxt', 'baizhan', 'it'];
```

两端的方括号是数组的标志。`sxt`是0号位置，`baizhan`是1号位置，`it`是2号位置。（位置也被称为下标）

除了在定义时赋值，数组也可以先定义后赋值。

```javascript
var arr = [];


arr[0] = 'sxt';
arr[1] = 'baizhan';
arr[2] = 'it';

```

任何类型的数据，都可以放入数组

```javascript
var arr = [ 100, [1, 2, 3],false ];
```

如果数组的元素还是数组，就形成了多维数组

```javascript
var a = [[1, 2], [3, 4]];
a[0][1] // 2
a[1][1] // 4

```

### length 属性

数组的length属性，返回数组的成员数量

```javascript
['sxt', 'baizhan', 'it'].length // 3
```

**实时效果反馈**

**1. 下列关于数组的操作，输出结果是：**

```javascript
var arr = [ 'sxt', 'baizhan', 'it' ];
console.log(arr[5])
```

A 0

B []

C undefined

D ""

**答案**

1=>C

##  XII、数组的遍历

![image-20220513185439156](https://www.itbaizhan.com/wiki/imgs/image-20220513185439156.png)

**数组的遍历可以考虑使用for循环或while循环**

```javascript
var a = ['sxt', 'baizhan', 'it'];


// for循环
for(var i = 0; i < a.length; i++) {
  console.log(a[i]);
}


// while循环
var i = 0;
while (i < a.length) {
  console.log(a[i]);
  i++;
}

```



**for...in遍历数组**

```javascript
var a = ['sxt', 'baizhan', 'it'];


for (var i in a) {
  console.log(a[i]);
}

```

**实时效果反馈**

**1. 下列遍历数组的操作中，画横线的地方应该填写的代码是：**

```javascript
var arr = ["尚学堂", 100, true];
for (var i = 0; i < ___; i++) {
    console.log(arr[i]);
}

```

A arr

B 10

C length

D arr.length

**答案**

1=>D

## XIII、 数组方法

### 1、数组静态方法_Array.isArray()

![image-20220513185558246](https://www.itbaizhan.com/wiki/imgs/image-20220513185558246.png)

`Array.isArray`方法返回一个布尔值，表示参数是否为数组。它可以弥补`typeof`运算符的不足

```
var arr = ["尚学堂", 100, true];
console.log(typeof arr); // object
```

```javascript
var arr = ['sxt', 'baizhan', 'it'];
Array.isArray(arr) // true

```

**实时效果反馈**

**1. 下列代码输出分别是？：**

```javascript
var arr = ["尚学堂", 100, true];
var str = "itbaizhan";
console.log(typeof arr);
console.log(Array.isArray(arr));
console.log(typeof str);
console.log(Array.isArray(str));

```

A object false string false

B object true string true

C object true false false

D object true string false

**答案**

1=>D

###  2、数组方法_push()/pop()

![image-20220513185750363](https://www.itbaizhan.com/wiki/imgs/image-20220513185750363.png)

`push`方法用于在数组的末端添加一个或多个元素，并返回添加新元素后的数组长度。注意，该方法会改变原数组

```javascript
var arr = [];
arr.push("尚学堂") // 1
arr.push('itbaizhan') // 2
arr.push(true, {}) // 4
arr // [尚学堂, 'itbaizhan', true, {}]

```

`pop`方法用于删除数组的最后一个元素，并返回该元素。注意，该方法会改变原数组

```javascript
var arr = ['尚学堂', 'itbaizhan', 'WEB前端'];


arr.pop() // 'WEB前端'
arr // ['尚学堂', 'itbaizhan']

```

**实时效果反馈**

**1. 下列关于数组输出的结果是：**

```javascript
var arr = [];
arr.push('尚学堂', 'itbaizhan');
arr.push('WEB前端');
arr.pop();
arr.push('尚学堂');
console.log(arr);

```

A `['尚学堂', 'itbaizhan', '尚学堂']`

B `['尚学堂', 'itbaizhan', 'WEB前端']`

C `['尚学堂', 'itbaizhan']`

D `['尚学堂', 'WEB前端']`

**答案**

1=>A

###  3、数组方法_shift()/unshift()

![image-20220513185937809](https://www.itbaizhan.com/wiki/imgs/image-20220513185937809.png)

`shift`方法用于删除数组的第一个元素，并返回该元素。注意，该方法会改变原数组

```javascript
var arr = ['尚学堂', 'itbaizhan', 'WEB前端'];


arr.shift() // '尚学堂'
arr // ['itbaizhan', 'WEB前端']

```

`shift`方法可以遍历并清空一个数组

```javascript
var list = [1, 2, 3, 4, 5, 6];
var item;


while (item = list.shift()) {
  console.log(item);
}


list // []

```

`unshift`方法用于在数组的第一个位置添加元素，并返回添加新元素后的数组长度。注意，该方法会改变原数组

```javascript
var arr = ['尚学堂', 'itbaizhan', 'WEB前端'];


arr.unshift('baizhan'); // 4
arr // ['baizhan', '尚学堂', 'itbaizhan', 'WEB前端']

```

`unshift`方法可以接受多个参数，这些参数都会添加到目标数组头部

```javascript
var arr = [ '尚学堂', 'itbaizhan' ];
arr.unshift('WEB前端', 'baizhan') // 4
arr // [ 'WEB前端', 'baizhan', '尚学堂', 'itbaizhan' ]

```

**实时效果反馈**

**1. 下列关于数组输出的结果是：**

```javascript
var arr = [];
arr.unshift('尚学堂', 'itbaizhan');
arr.unshift('WEB前端');
arr.shift();
arr.unshift('尚学堂');
console.log(arr);

```

A `['尚学堂', '尚学堂', 'itbaizhan']`

B `['尚学堂', 'itbaizhan', 'WEB前端']`

C `['尚学堂', 'itbaizhan']`

D `['尚学堂', 'WEB前端']`

**答案**

1=>A

### 4、数组方法_join()

![image-20220513190055766](https://www.itbaizhan.com/wiki/imgs/image-20220513190055766.png)

`join`方法以指定参数作为分隔符，将所有数组成员连接为一个字符串返回。如果不提供参数，默认用逗号分隔

```javascript
var a = [1, 2, 3, 4];


a.join(' ') // '1 2 3 4'
a.join(' | ') // "1 | 2 | 3 | 4"
a.join() // "1,2,3,4"

```

如果数组成员是`undefined`或`null`或空位，会被转成空字符串

```javascript
[undefined, null].join('#')
// '#'


['a',, 'b'].join('-')
// 'a--b'

```

数组的`join`配合字符串的`split`可以实现数组与字符串的互换

```javascript
var arr = ["a","b","c"];
var myArr = arr.join("");
console.log(myArr);
console.log(myArr.split(""));

```

**实时效果反馈**

**1. 下列关于数组输出的结果是：**

```javascript
var arr = ["尚学堂","百战程序员"];
var myArr = arr.join("");
console.log(myArr);
console.log(myArr.split(""));

```

A 尚学堂百战程序员 ["尚学堂","百战程序员"]

B 尚学堂百战程序员 ['尚', '学', '堂', '百', '战', '程', '序', '员']

C ["尚学堂","百战程序员"] 尚学堂百战程序员

D ['尚', '学', '堂', '百', '战', '程', '序', '员'] 尚学堂百战程序员

**答案**

1=>B

###  5、数组方法_concat()

![image-20220513190402634](https://www.itbaizhan.com/wiki/imgs/image-20220513190402634.png)

`concat`方法用于多个数组的合并。它将新数组的成员，添加到原数组成员的后部，然后返回一个新数组，原数组不变

```javascript
['hello'].concat(['world'])
// ["hello", "world"]


['hello'].concat(['world'], ['!'])
// ["hello", "world", "!"]

```

除了数组作为参数，`concat`也接受其他类型的值作为参数，添加到目标数组尾部。

```javascript
[1, 2, 3].concat(4, 5, 6)
// [1, 2, 3, 4, 5, 6]

```

> **应用场景**
>
> 上拉加载，合并数据

**实时效果反馈**

**1. 下列关于数组输出的结果是：**

```javascript
[1, 2, 3].concat(4, 5, 6,[7,8,9])
```

A `[1, 2, 3, 4, 5, 6]`

B `[1, 2, 3, 4, 5, 6, [7, 8, 9]]`

C `[1, 2, 3, 4, 5, 6, 7, 8, 9]`

D `[1, 2, 3, 4, 5, 6][7, 8, 9]`

**答案**

1=>C

###  6、数组方法_reverse()

![image-20220513190443734](https://www.itbaizhan.com/wiki/imgs/image-20220513190443734.png)

`reverse`方法用于颠倒排列数组元素，返回改变后的数组。注意，该方法将改变原数组

```javascript
var a = ['a', 'b', 'c'];


a.reverse() // ["c", "b", "a"]
a // ["c", "b", "a"]

```

实现一个字符串反转排列

```javascript
var str = "hello";
str.split("").reverse().join("")

```

**实时效果反馈**

**1. 下列关于数组输出的结果是：**

```javascript
var str = "hello";
str.split("").reverse().join("-");

```

A olleh

B hello

C 'o-l-l-e-h'

D 'h-e-l-l-o'

**答案**

1=>C

###  7、数组方法_indexOf()

![image-20220513190744950](https://www.itbaizhan.com/wiki/imgs/image-20220513190744950.png)

```javascript
var arr = ['a', 'b', 'c'];


arr.indexOf('b') // 1
arr.indexOf('y') // -1

```



`indexOf`方法还可以接受第二个参数，表示搜索的开始位置

```javascript
['尚学堂', '百战程序员', 'itbaizhan'].indexOf('尚学堂', 1) // -1
```

**实时效果反馈**

**1. 下列关于数组方法，运行正确结果是：**

```javascript
var arr = ["尚学堂", "it", "itbaizhan","it"];
arr.indexOf("it",2)
```

A -1

B 1

C 3

D undefined

**答案**

1=>B

## XIV、函数

![image-20211024114220828](https://www.itbaizhan.com/wiki/imgs/image-20211024114220828.png)

函数是一段可以反复调用的代码块

### 函数的声明

function 命令： function命令声明的代码区块，就是一个函数。function命令后面是函数名，函数名后面是一对圆括号，里面是传入函数的参数。函数体放在大括号里面。

```javascript
function print(s) {
  console.log(s);
}

```

### 函数名的提升

JavaScript 引擎将函数名视同变量名，所以采用function命令声明函数时，整个函数会像变量声明一样，被提升到代码头部

```javascript
add();


function add() {}

```

### 函数参数

函数运行的时候，有时需要提供外部数据，不同的外部数据会得到不同的结果，这种外部数据就叫参数

```javascript
function square(x) {
    console.log(x * x);
}


square(2) // 4
square(3) // 9

```

### 函数返回值

JavaScript函数提供两个接口实现与外界的交互，其中参数作为入口，接收外界信息；返回值作为出口，把运算结果反馈给外界

```javascript
function getName(name){
    return name;
}


var myName = getName("itbaizhan")
console.log(myName); // itbaizhan

```

> **温馨提示**
>
> `return` 后面不能在添加任何代码，因为不会执行

**实时效果反馈**

**1. 下列函数执行输出“itbaizhan”，横线处应该填写的代码是：**

```javascript
function getName(name) {
    ___;
}
var myName = getName("itbaizhan")
console.log(myName); // itbaizhan

```

A return name

B return

C name

D return "itbaizhan"

**答案**

1=>A

##  XV、对象

### 1、对象概述

![image-20211025120047650](https://www.itbaizhan.com/wiki/imgs/image-20211025120047650.png)

什么是对象？对象（object）是 JavaScript 语言的核心概念，也是最重要的数据类型

简单说，对象就是一组“键值对”（key-value）的集合，是一种无序的复合数据集合

![image-20211025173456785](https://www.itbaizhan.com/wiki/imgs/image-20211025173456785.png)

```javascript
var user = {
  name: 'itbaizhan',
  age: '13'
};

```

对象的每一个键名又称为“属性”（property），它的“键

值”可以是任何数据类型。如果一个属性的值为函数，通常把这个属性称为“方法”，它可以像函数那样调用

```javascript
var user = {
  getName: function (name) {
    return name;
  }
};
user.getName("itbaizhan") // itbaizhan

```

如果属性的值还是一个对象，就形成了链式引用

```javascript
var user = {
    name:"itbaizhan",
    age:13,
    container:{
        frontEnd:["Web前端","Android","iOS"],
        backEnd:["Java","Python"]
    }
}
user.container.frontEnd // ["Web前端","Android","iOS"]

```

**实时效果反馈**

**1. 下列关于对象描述正确的是：**

A 对象是条件语句，负责进行判断

B 对象是一段反复调用的代码块

C 对象就是一组“键值对”（key-value）的集合

D 对象是按次序排列的一组值。每个值的位置都有编号（从0开始）

**答案**

1=>C

###  2、Math对象

![image-20220516161116265](https://www.itbaizhan.com/wiki/imgs/image-20220516161116265.png)

Math是 JavaScript 的原生对象，提供各种数学功能。

#### Math.abs()

**`Math.abs`方法返回参数值的绝对值**

```javascript
Math.abs(1) // 1
Math.abs(-1) // 1

```

#### Math.max()，Math.min()

`Math.max`方法返回参数之中最大的那个值，`Math.min`返回最小的那个值。如果参数为空, `Math.min`返回`Infinity`, `Math.max`返回`-Infinity`。

```javascript
Math.max(2, -1, 5) // 5
Math.min(2, -1, 5) // -1
Math.min() // Infinity
Math.max() // -Infinity

```

#### Math.floor()，Math.ceil()

`Math.floor`方法返回小于参数值的最大整数

```javascript
Math.floor(3.2) // 3
Math.floor(-3.2) // -4

```

`Math.ceil`方法返回大于参数值的最小整数

```javascript
Math.ceil(3.2) // 4
Math.ceil(-3.2) // -3

```

#### Math.random()

`Math.random()`返回0到1之间的一个伪随机数，可能等于0，但是一定小于1

```javascript
Math.random() // 0.28525367438365223
```

任意范围的随机数生成函数如下

```javascript
function getRandomArbitrary(min, max) {
  return Math.random() * (max - min) + min;
}


getRandomArbitrary(5, 10)

```

**实时效果反馈**

**1. 下列代码获得一个正整数，横线处应该填写的内容是：**

```javascript
function ToInteger(x) {
    x = Number(x);
    return ___(___(x));
}
ToInteger(-10.4); // 向下取整：10

```

A `Math.floor` `Math.abs`

B `Math.ceil` `Math.abs`

C `Math.ceil` `Math.min`

D `Math.floor` `Math.min`

**答案**

1=>A

###  3、Date对象

![img](https://www.itbaizhan.com/wiki/imgs/SNAGHTML2e8d011c.PNG)

`Date`对象是 JavaScript 原生的时间库。它以1970年1月1日00:00:00作为时间的零点，可以表示的时间范围是前后各1亿天（单位为毫秒）

#### Date.now()

`Date.now`方法返回当前时间距离时间零点（1970年1月1日 00:00:00 UTC）的毫秒数，相当于 Unix 时间戳乘以1000

```javascript
Date.now();   // 1635216733395
```

#### 时间戳

时间戳是指格林威治时间1970年01月01日00时00分00秒(北京时间1970年01月01日08时00分00秒)起至现在的总秒数。

格林威治和北京时间就是时区的不同

Unix是20世纪70年代初出现的一个操作系统，Unix认为1970年1月1日0点是时间纪元。JavaScript也就遵循了这一约束

`Date`对象提供了一系列`get*`方法，用来获取实例对象某个方面的值

> **实例方法get类**
>
> getTime()：返回实例距离1970年1月1日00:00:00的毫秒数 getDate()：返回实例对象对应每个月的几号（从1开始） getDay()：返回星期几，星期日为0，星期一为1，以此类推 getYear()：返回距离1900的年数 getFullYear()：返回四位的年份 getMonth()：返回月份（0表示1月，11表示12月） getHours()：返回小时（0-23） getMilliseconds()：返回毫秒（0-999） getMinutes()：返回分钟（0-59） getSeconds()：返回秒（0-59）

```javascript
var d = new Date('January 6, 2022');
d.getDate() // 6
d.getMonth() // 0
d.getYear() // 122
d.getFullYear() // 2022

```

编写函数获得本年度剩余天数

```javascript
function leftDays() {
  var today = new Date();
  var endYear = new Date(today.getFullYear(), 11, 31, 23, 59, 59, 999);
  var msPerDay = 24 * 60 * 60 * 1000;
  return Math.round((endYear.getTime() - today.getTime()) / msPerDay);
}

```

**实时效果反馈**

**1. 下列代码计算本年度剩余天数，划横线处应该填写代码是：**

```javascript
function leftDays() {
  var today = new Date();
  var endYear = new Date(today.___, 11, 31, 23, 59, 59, 999);
  var msPerDay = 24 * 60 * 60 * 1000;
  return Math.round((endYear.___ - today.___) / msPerDay);
}

```

A getTime() getDate() getTime()

B getTime() getTime() getDate()

C getFullYear() getTime() getDate()

D getFullYear() getTime() getTime()

**答案**

1=>D

### 4、DOM概述

![image-20211027144734355](https://www.itbaizhan.com/wiki/imgs/image-20211027144734355.png)

DOM 是 JavaScript 操作网页的接口，全称为“文档对象模型”（Document Object Model）。它的作用是将网页转为一个 JavaScript 对象，从而可以用脚本进行各种操作（比如对元素增删内容）

浏览器会根据 DOM 模型，将结构化文档HTML解析成一系列的节点，再由这些节点组成一个树状结构（DOM Tree）。所有的节点和最终的树状结构，都有规范的对外接口

DOM 只是一个接口规范，可以用各种语言实现。所以严格地说，DOM 不是 JavaScript 语法的一部分，但是 DOM 操作是 JavaScript 最常见的任务，离开了 DOM，JavaScript 就无法控制网页。另一方面，JavaScript 也是最常用于 DOM 操作的语言

#### 节点

DOM 的最小组成单位叫做节点（node）。文档的树形结构（DOM 树），就是由各种不同类型的节点组成。每个节点可以看作是文档树的一片叶子

![image-20211027131821279](https://www.itbaizhan.com/wiki/imgs/image-20211027131821279.png)

节点的类型有七种

> Document：整个文档树的顶层节点 DocumentType：doctype标签 Element：网页的各种HTML标签 Attribute：网页元素的属性（比如class="right"） Text：标签之间或标签包含的文本 Comment：注释 DocumentFragment：文档的片段

#### 节点树

一个文档的所有节点，按照所在的层级，可以抽象成一种树状结构。这种树状结构就是 DOM 树。它有一个顶层节点，下一层都是顶层节点的子节点，然后子节点又有自己的子节点，就这样层层衍生出一个金字塔结构，倒过来就像一棵树

浏览器原生提供document节点，代表整个文档

```
1
document
2
// 整个文档树
```

除了根节点，其他节点都有三种层级关系

> 父节点关系（parentNode）：直接的那个上级节点 子节点关系（childNodes）：直接的下级节点 同级节点关系（sibling）：拥有同一个父节点的节点

#### Node.nodeType属性

不同节点的nodeType属性值和对应的常量如下

> 文档节点（document）：9，对应常量Node.DOCUMENT_NODE 元素节点（element）：1，对应常量Node.ELEMENT_NODE 属性节点（attr）：2，对应常量Node.ATTRIBUTE_NODE 文本节点（text）：3，对应常量Node.TEXT_NODE 文档片断节点（DocumentFragment）：11，对应常量Node.DOCUMENT_FRAGMENT_NODE

```
1
document.nodeType // 9
2
document.nodeType === Node.DOCUMENT_NODE // true
```

**实时效果反馈**

**1. 下列那个不是节点类型：**

A Document

B Element

C Attribute

D Array

**答案**

1=>D

###  5、document对象_方法/获取元素

![image-20211027150914322](https://www.itbaizhan.com/wiki/imgs/image-20211027150914322.png)

#### document.getElementsByTagName()

`document.getElementsByTagName`方法搜索 HTML 标签名，返回符合条件的元素。它的返回值是一个类似数组对象（`HTMLCollection`实例），可以实时反映 HTML 文档的变化。如果没有任何匹配的元素，就返回一个空集

```
1
var paras = document.getElementsByTagName('p');
```

如果传入`*`，就可以返回文档中所有 HTML 元素

```
1
var allElements = document.getElementsByTagName('*');
```

#### document.getElementsByClassName()

`document.getElementsByClassName`方法返回一个类似数组的对象（`HTMLCollection`实例），包括了所有`class`名字符合指定条件的元素，元素的变化实时反映在返回结果中

```
1
var elements = document.getElementsByClassName(names);
```

由于`class`是保留字，所以 JavaScript 一律使用`className`表示 CSS 的`class`

参数可以是多个`class`，它们之间使用空格分隔

```
1
var elements = document.getElementsByClassName('foo bar');
```

#### document.getElementsByName()

`document.getElementsByName`方法用于选择拥有`name`属性的 HTML 元素（比如`<form>`、`<radio>`、`<img>`等），返回一个类似数组的的对象（`NodeList`实例），因为`name`属性相同的元素可能不止一个

```
1
// 表单为 <form name="itbaizhan"></form>
2
var forms = document.getElementsByName('itbaizhan');
```

#### document.getElementById()

```
document.getElementById`方法返回匹配指定`id`属性的元素节点。如果没有发现匹配的节点，则返回`null
1
var elem = document.getElementById('para1');
```

注意，该方法的参数是大小写敏感的。比如，如果某个节点的`id`属性是`main`，那么`document.getElementById('Main')`将返回`null`

#### document.querySelector()

```
document.querySelector`方法接受一个 CSS 选择器作为参数，返回匹配该选择器的元素节点。如果有多个节点满足匹配条件，则返回第一个匹配的节点。如果没有发现匹配的节点，则返回`null
1
var el1 = document.querySelector('.myclass');
```

#### document.querySelectorAll()

`document.querySelectorAll`方法与`querySelector`用法类似，区别是返回一个`NodeList`对象，包含所有匹配给定选择器的节点

```
1
var elementList = document.querySelectorAll('.myclass');
```

**实时效果反馈**

**1. 以下那个是通过ID获取元素对象：**

A getElementById

B getElementsByTagName

C getElementsByClassName

D getElementsByName

**2. 以下那个是通过Class获取元素对象：**

A getElementById

B getElementsByTagName

C getElementsByClassName

D getElementsByName

**答案**

1=>A 2=>C

###  6、document对象_方法/创建元素

![image-20211027151634674](https://www.itbaizhan.com/wiki/imgs/image-20211027151634674.png)

#### document.createElement()

`document.createElement`方法用来生成元素节点，并返回该节点

```
1
var newDiv = document.createElement('div');
```

#### document.createTextNode()

`document.createTextNode`方法用来生成文本节点（`Text`实例），并返回该节点。它的参数是文本节点的内容

```
1
var newDiv = document.createElement('div');
2
var newContent = document.createTextNode('Hello');
3
newDiv.appendChild(newContent);
```

#### document.createAttribute()

`document.createAttribute`方法生成一个新的属性节点（`Attr`实例），并返回它

```
1
var attribute = document.createAttribute(name);
1
var root = document.getElementById('root');
2
var it = document.createAttribute('itbaizhan');
3
it.value = 'it';
4
root.setAttributeNode(it);
```

**实时效果反馈**

**1. 下列代码是创建元素，并添加内容，横线处应该填写的内容是：**

```
1
var newDiv = document.createElement('div');
2
var newContent = document.____('Hello');
3
newDiv.appendChild(newContent);
```

A createElement

B appendChild

C createAttribute

D createTextNode

**答案**

1=>D

###  7、Element对象_属性

![image-20211027202346912](https://www.itbaizhan.com/wiki/imgs/image-20211027202346912.png)

Element对象对应网页的 HTML 元素。每一个 HTML 元素，在 DOM 树上都会转化成一个Element节点对象（以下简称元素节点）

#### Element.id

`Element.id`属性返回指定元素的`id`属性，该属性可读写

```
1
// HTML 代码为 <p id="foo">
2
var p = document.querySelector('p');
3
p.id // "foo"
```

#### Element.className

`className`属性用来读写当前元素节点的`class`属性。它的值是一个字符串，每个`class`之间用空格分割

```
1
// HTML 代码 <div class="one two three" id="myDiv"></div>
2
var div = document.getElementById('myDiv');
3
div.className
```

#### Element.classList

`classList`对象有下列方法

> - `add()`：增加一个 class。
> - `remove()`：移除一个 class。
> - `contains()`：检查当前元素是否包含某个 class。
> - `toggle()`：将某个 class 移入或移出当前元素。

```
1
var div = document.getElementById('myDiv');
2
3
div.classList.add('myCssClass');
4
div.classList.add('foo', 'bar');
5
div.classList.remove('myCssClass');
6
div.classList.toggle('myCssClass'); // 如果 myCssClass 不存在就加入，否则移除
7
div.classList.contains('myCssClass'); // 返回 true 或者 false
```

#### Element.innerHTML

`Element.innerHTML`属性返回一个字符串，等同于该元素包含的所有 HTML 代码。该属性可读写，常用来设置某个节点的内容。它能改写所有元素节点的内容，包括`<HTML>`和`<body>`元素

```
1
el.innerHTML = '';
```

#### Element.innerText

`innerText`和`innerHTML`类似，不同的是`innerText`无法识别元素，会直接渲染成字符串

**实时效果反馈**

**1. 下列代码为div元素动态添加一个class，画横线处应该填写的内容是：**

```
1
var div = document.getElementById('myDiv');
2
div.classList.___('myCssClass');
```

A remove

B add

C toggle

D contains

**答案**

1=>B

###  8、Element获取元素位置

| 属性         |                             描述                             |
| :----------- | :----------------------------------------------------------: |
| clientHeight | 获取元素高度包括`padding`部分，但是不包括`border`、`margin`  |
| clientWidth  | 获取元素宽度包括`padding`部分，但是不包括`border`、`margin`  |
| scrollHeight | 元素总高度，它包括`padding`，但是不包括`border`、`margin`包括溢出的不可见内容 |
| scrollWidth  | 元素总宽度，它包括`padding`，但是不包括`border`、`margin`包括溢出的不可见内容 |
| scrollLeft   |              元素的水平滚动条向右滚动的像素数量              |
| scrollTop    |              元素的垂直滚动条向下滚动的像素数量              |
| offsetHeight | 元素的 CSS 垂直高度（单位像素），包括元素本身的高度、padding 和 border |
| offsetWidth  | 元素的 CSS 水平宽度（单位像素），包括元素本身的高度、padding 和 border |
| offsetLeft   |                    到定位父级左边界的间距                    |
| offsetTop    |                    到定位父级上边界的间距                    |

#### Element.clientHeight，Element.clientWidth

`Element.clientHeight`属性返回一个整数值，表示元素节点的 CSS 高度（单位像素），只对块级元素生效，对于行内元素返回`0`。如果块级元素没有设置 CSS 高度，则返回实际高度

除了元素本身的高度，它还包括`padding`部分，但是不包括`border`、`margin`。如果有水平滚动条，还要减去水平滚动条的高度。注意，这个值始终是整数，如果是小数会被四舍五入。

`Element.clientWidth`属性返回元素节点的 CSS 宽度，同样只对块级元素有效，也是只包括元素本身的宽度和`padding`，如果有垂直滚动条，还要减去垂直滚动条的宽度。

`document.documentElement`的`clientHeight`属性，返回当前视口的高度（即浏览器窗口的高度）。`document.body`的高度则是网页的实际高度。

```
1
// 视口高度
2
document.documentElement.clientHeight
3
4
// 网页总高度
5
document.body.clientHeight
```

#### Element.scrollHeight，Element.scrollWidth

`Element.scrollHeight`属性返回一个整数值（小数会四舍五入），表示当前元素的总高度（单位像素），它包括`padding`，但是不包括`border`、`margin`以及水平滚动条的高度（如果有水平滚动条的话）

`Element.scrollWidth`属性表示当前元素的总宽度（单位像素），其他地方都与`scrollHeight`属性类似。这两个属性只读

整张网页的总高度可以从`document.documentElement`或`document.body`上读取

```
1
// 返回网页的总高度
2
document.documentElement.scrollHeight
3
document.body.scrollHeight
```

#### Element.scrollLeft，Element.scrollTop

`Element.scrollLeft`属性表示当前元素的水平滚动条向右侧滚动的像素数量，`Element.scrollTop`属性表示当前元素的垂直滚动条向下滚动的像素数量。对于那些没有滚动条的网页元素，这两个属性总是等于0

如果要查看整张网页的水平的和垂直的滚动距离，要从`document.documentElement`元素上读取

```
1
document.documentElement.scrollLeft
2
document.documentElement.scrollTop
```

#### Element.offsetHeight，Element.offsetWidth

`Element.offsetHeight`属性返回一个整数，表示元素的 CSS 垂直高度（单位像素），包括元素本身的高度、padding 和 border，以及水平滚动条的高度（如果存在滚动条）。

`Element.offsetWidth`属性表示元素的 CSS 水平宽度（单位像素），其他都与`Element.offsetHeight`一致。

这两个属性都是只读属性，只比`Element.clientHeight`和`Element.clientWidth`多了边框的高度或宽度。如果元素的 CSS 设为不可见（比如`display: none;`），则返回`0`

#### Element.offsetLeft，Element.offsetTop

`Element.offsetLeft`返回当前元素左上角相对于`Element.offsetParent`节点的水平位移，`Element.offsetTop`返回垂直位移，单位为像素。通常，这两个值是指相对于父节点的位移

```html
<div class="parent">
    <div class="box" id="box"></div>
</div>
.parent{
    width: 200px;
    height: 200px;
    background: red;
    position: relative;
    left: 50px;
    top: 50px;
}


.box{
    width: 100px;
    height: 100px;
    background: yellow;
    position: relative;
    left: 50px;
    top: 50px;
}
<script>
var box = document.getElementById("box");
console.log(box.offsetLeft);
console.log(box.offsetTop);
</script>
```

**实时效果反馈**

**1. 下面是获得整个视口的宽度和高度：**

```
1
document.documentElement.___
2
document.documentElement.___
```

A offsetLeft offsetTop

B scrollHeight scrollWidth

C clientLeft clientTop

**2. 以下哪个是获得元素的高度，包含内外边距和边框：**

A offsetLeft offsetTop

B offsetHeight offsetWidth

C clientLeft clientTop

D clientHeight clientWidth

**答案**

1=>B 2=>B

###  9、CSS操作

![image-20211102152242203](https://www.itbaizhan.com/wiki/imgs/image-20211102152242203.png)

#### `HTML` 元素的 `style` 属性

操作 CSS 样式最简单的方法，就是使用网页元素节点的`setAttribute`方法直接操作网页元素的`style`属性

```javascript
div.setAttribute(
  'style',
  'background-color:red;' + 'border:1px solid black;'
);

```

#### 元素节点的`style`属性

```javascript
var divStyle = document.querySelector('div').style;


divStyle.backgroundColor = 'red';
divStyle.border = '1px solid black';
divStyle.width = '100px';
divStyle.height = '100px';
divStyle.fontSize = '10em';

```

#### `cssText`属性

```javascript
var divStyle = document.querySelector('div').style;


divStyle.cssText = 'background-color: red;'
  + 'border: 1px solid black;'
  + 'height: 100px;'
  + 'width: 100px;';

```

**实时效果反馈**

**1. 下列是设置样式的代码，横线处应该填写的代码是：**

```
1
var divStyle = document.querySelector('div');
2
divStyle.___.backgroundColor = 'red';
```

A `style`

B `cssText`

C `setAttribute`

D `getAttribute`

**答案**

1=>A

##  XVI、事件处理程序

![image-20211101185525155](https://www.itbaizhan.com/wiki/imgs/image-20211101185525155.png)

事件处理程序分为：

1. HTML事件处理
2. DOM0级事件处理
3. DOM2级事件处理

### HTML事件

```html
<!DOCTYPE html>
<html>
    <head lang="en">
        <meta charset="UTF-8">
        <title>Js事件详解--事件处理</title>
    </head>
    <body>
        <div id="div">
            <button id="btn1" onclick="demo()">按钮</button>
        </div>
        <script>
            function demo(){
                alert("hello html事件处理");
            }
        </script>
    </body>
</html> 

```

### DOM0级事件处理

```html
<body>
    <div id="div">
        <button id="btn1">按钮</button>
    </div>
    <script>
        var btn1=document.getElementById("btn1");
        btn1.onclick=function(){alert("Hello DOM0级事件处理程序1");}//被覆盖掉
        btn1.onclick=function(){alert("Hello DOM0级事件处理程序2");}
    </script>
</body>

```

### DOM2级事件处理

```html
<body>
    <div id="div">
        <button id="btn1">按钮</button>
    </div>
    <script>
        var btn1=document.getElementById("btn1");
        btn1.addEventListener("click",demo1);
        btn1.addEventListener("click",demo2);
        btn1.addEventListener("click",demo3);
        function demo1(){
            alert("DOM2级事件处理程序1")
        }
        function demo2(){
            alert("DOM2级事件处理程序2")
        }
        function demo3(){
            alert("DOM2级事件处理程序3")
        }
        btn1.removeEventListener("click",demo2);
    </script>
</body>

```

**实时效果反馈**

**1. 下列代码，是属于哪种事件处理方式：**

```
1
btn2.addEventListener('click',function(){
2
    console.log("触发事件");
3
})
```

A HTML事件

B DOM0级事件处理

C DOM2级事件处理

D IE事件处理程序

**答案**

1=>C

##  XVII、事件类型之鼠标事件

![image-20211102113124027](https://www.itbaizhan.com/wiki/imgs/image-20211102113124027.png)

### 鼠标事件

鼠标事件指与鼠标相关的事件，具体的事件主要有以下一些

1. click：按下鼠标时触发
2. dblclick：在同一个元素上双击鼠标时触发
3. mousedown：按下鼠标键时触发
4. mouseup：释放按下的鼠标键时触发
5. mousemove：当鼠标在节点内部移动时触发。当鼠标持续移动时，该事件会连触发。
6. mouseenter：鼠标进入一个节点时触发，进入子节点不会触发这个事件
7. mouseleave：鼠标离开一个节点时触发，离开父节点不会触发这个事件
8. mouseover：鼠标进入一个节点时触发，进入子节点会再一次触发这个事件
9. mouseout：鼠标离开一个节点时触发，离开父节点也会触发这个事件
10. wheel：滚动鼠标的滚轮时触发

```javascript
var btn1 = document.getElementById("btn1");
btn1.onclick = function(){
    console.log("click事件");
}

```

> **温馨提示**
>
> 这些方法在使用的时候，除了DOM2级事件，都需要添加前缀`on`

**实时效果反馈**

**1. 下列代码是鼠标事件，划横线处应该填写的是：**

```javascript
// 需求：鼠标在元素内移动，会一直触发事件
var box = document.getElementById("box");
box.___ = function(){
    console.log("事件在元素上会一直触发");
}

```

A `onclick`

B `onmouseover`

C `onmousemove`

D `onmouseenter`

**答案**

1=>C

##  XVIII、Event事件对象

![image-20211102132626706](https://www.itbaizhan.com/wiki/imgs/image-20211102132626706.png)

事件发生以后，会产生一个事件对象，作为参数传给监听函数。

### Event对象属性

1. Event.Target
2. Event.type

#### Event.target

Event.target属性返回事件当前所在的节点

```javascript
// HTML代码为
// <p id="para">Hello</p>
function setColor(e) {
  console.log(this === e.target);
  e.target.style.color = 'red';
}


para.addEventListener('click', setColor);

```

#### Event.type

Event.type属性返回一个字符串，表示事件类型。事件的类型是在生成事件的时候。该属性只读

### Event对象方法

1. Event.preventDefault()
2. Event.stopPropagation()

#### Event.preventDefault

Event.preventDefault方法取消浏览器对当前事件的默认行为。比如点击链接后，浏览器默认会跳转到另一个页面，使用这个方法以后，就不会跳转了

```javascript
btn.onclick = function(e){
    e.preventDefault(); // 阻止默认事件
    console.log("点击A标签");
}

```

#### Event.stopPropagation()

stopPropagation方法阻止事件在 DOM 中继续传播，防止再触发定义在别的节点上的监听函数，但是不包括在当前节点上其他的事件监听函数

```javascript
btn.onclick = function(e){
    e.stopPropagation(); // 阻止事件冒泡
    console.log("btn");
}

```

**实时效果反馈**

**1. 下列关于阻止默认事件方法正确的是：**

A stopPropagation()

B preventDefault()

C target

D currentTarget

**答案**

1=>B

##  XIX、事件类型之键盘事件

![image-20211102134118599](https://www.itbaizhan.com/wiki/imgs/image-20211102134118599.png)

键盘事件由用户击打键盘触发，主要有keydown、keypress、keyup三个事件

1. keydown：按下键盘时触发。
2. keypress：按下有值的键时触发，即按下 Ctrl、Alt、Shift、Meta 这样无值的键，这个事件不会触发。对于有值的键，按下时先触发keydown事件，再触发这个事件。
3. keyup：松开键盘时触发该事件

```javascript
username.onkeypress = function(e){
    console.log("keypress事件");
}

```

### event对象

keyCode:唯一标识

```javascript
var username = document.getElementById("username");
username.onkeydown = function(e){
    if(e.keyCode === 13){
        console.log("回车");
    }
}

```

**实时效果反馈**

**1. 下列那个不是键盘事件：**

A keydown

B keypress

C keyup

D click

**答案**

1=>D

##  XX、事件类型之表单事件

![image-20211102134851713](https://www.itbaizhan.com/wiki/imgs/image-20211102134851713.png)

表单事件是在使用表单元素及输入框元素可以监听的一系列事件

1. input事件
2. select事件
3. Change事件
4. reset事件
5. submit事件

### input事件

input事件当`<input>、<select>、<textarea>`的值发生变化时触发。对于复选框（`<input type=checkbox>`）或单选框（`<input type=radio>`），用户改变选项时，也会触发这个事件

input事件的一个特点，就是会连续触发，比如用户每按下一次按键，就会触发一次input事件。

```js
var username = document.getElementById("username");
username.oninput = function(e){
    console.log(e.target.value);
}

```

### select事件

select事件当在`<input>、<textarea>`里面选中文本时触发

```js
// HTML 代码如下
// <input id="test" type="text" value="Select me!" />


var elem = document.getElementById('test');
elem.addEventListener('select', function (e) {
  console.log(e.type); // "select"
}, false);

```

### Change 事件

Change事件当`<input>、<select>、<textarea>`的值发生变化时触发。它与input事件的最大不同，就是不会连续触发，只有当全部修改完成时才会触发

```js
var email = document.getElementById("email");
email.onchange = function(e){
    console.log(e.target.value);
}

```

### reset 事件，submit 事件

这两个事件发生在表单对象`<form>`上，而不是发生在表单的成员上。

reset事件当表单重置（所有表单成员变回默认值）时触发。

submit事件当表单数据向服务器提交时触发。注意，submit事件的发生对象是`<form>`元素，而不是`<button>`元素，因为提交的是表单，而不是按钮

```js
<form id="myForm" onsubmit="submitHandle">
    <button onclick="resetHandle">重置数据</button>
    <button>提交</button>
</form>

```

```js
var myForm = document.getElementById("myForm")
function resetHandle(){
    myForm.reset();
}
function submitHandle(){
    console.log("提交");
}

```

**实时效果反馈**

**1. 下列代码中，横线处应该填写的内容是：**

```js
// 需求：用户每次输入都需要触发的事件
var username = document.getElementById("username");
username.___ = function(e){
    console.log(e.target.value);
}

```

A select

B oninput

C onchange

D submit

**答案**

1=>B

## XX·、事件代理(事件委托)

![image-20211102143218643](https://www.itbaizhan.com/wiki/imgs/image-20211102143218643.png)

由于事件会在冒泡阶段向上传播到父节点，因此可以把子节点的监听函数定义在父节点上，由父节点的监听函数统一处理多个子元素的事件。这种方法叫做事件的代理（delegation）

```html
var ul = document.querySelector('ul');


ul.addEventListener('click', function (event) {
  if (event.target.tagName.toLowerCase() === 'li') {
    // some code
  }
});

```

**实时效果反馈**

**1. 下列是关于事件代理的处理，横线处应该填写的代码是：**

```html
var parent = document.getElementById("parent");
parent.addEventListener("click",function(e){
    if(e.___.tagName.___ === 'li'){
        console.log(e.target.innerHTML);
    }
})

```

A target toUpperCase()

B target toLowerCase()

C currentTarget toLowerCase()

D currentTarget toUpperCase()

**答案**

1=>B

 

##  XXI、定时器之`setTimeout()`

![image-20211109102513172](https://www.itbaizhan.com/wiki/imgs/image-20211109102513172.png)

JavaScript 提供定时执行代码的功能，叫做定时器（timer），主要由`setTimeout()`和`setInterval()`这两个函数来完成。它们向任务队列添加定时任务

`setTimeout`函数用来指定某个函数或某段代码，在多少毫秒之后执行。它返回一个整数，表示定时器的编号，以后可以用来取消这个定时器。

```
1
var timerId = setTimeout(func|code, delay);
```

`setTimeout`函数接受两个参数，第一个参数`func|code`是将要推迟执行的函数名或者一段代码，第二个参数`delay`是推迟执行的毫秒数

```
setTimeout(function(){
    console.log("定时器")
},1000)
```

> **温馨提示**
>
> 还有一个需要注意的地方，如果回调函数是对象的方法，那么`setTimeout`使得方法内部的`this`关键字指向全局环境，而不是定义时所在的那个对象

```js
var name = "sxt";
var user = {
    name: "itbaizhan",
    getName: function () {
        setTimeout(function(){
            console.log(this.name);
        },1000)
    }
};
user.getName();

```

解决方案

```js
var name = "sxt";
var user = {
    name: "itbaizhan",
    getName: function () {
        var that = this;
        setTimeout(function(){
            console.log(that.name);
        },1000)
    }
};
user.getName();

```

定时器可以进行取消

```
1
var id = setTimeout(f, 1000);
2
clearTimeout(id);
```

**实时效果反馈**

**1. 以下是关于定时器`setTimeout`代码，运行结果是：**

```js
var name = "sxt";
var user = {
    name: "itbaizhan",
    getName: function () {
        var that = this;
        setTimeout(function(){
            console.log(that.name);
        },1000)
    }
};
user.getName();

```

A itbaizhan

B sxt

C 报错

D undefined

**答案**

1=>A

##  XXII、定时器之`setInterval()`

![image-20211109102842728](https://www.itbaizhan.com/wiki/imgs/image-20211109102842728.png)

`setInterval`函数的用法与`setTimeout`完全一致，区别仅仅在于`setInterval`指定某个任务每隔一段时间就执行一次，也就是无限次的定时执行

```js
var timer = setInterval(function() {
  console.log(2);
}, 1000)

```

通过setInterval方法实现网页动画

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #someDiv{
            width: 100px;
            height: 100px;
            background: red;
        }
    </style>
</head>
<body>
    <div id="someDiv"></div>
    <script>
        var div = document.getElementById('someDiv');
        var opacity = 1;
        var fader = setInterval(function() {
          opacity -= 0.05;
          if (opacity > 0) {
            div.style.opacity = opacity;
          } else {
            clearInterval(fader);
          }
        }, 30);


    </script>
</body>
</html>

```

定时器可以进行取消

```
var id = setInterval(f, 1000);
clearInterval(id);

```

**实时效果反馈**

**1. 以下是关于定时器`setInterval`代码，每秒打印当前时间，横线处填写代码是：**

```
___(function(){
    console.log(new Date().toLocaleTimeString());
},1000)

```

A getTime

B setTimeout

C setInterval

D function

**答案**

1=>C

##  XXIII、防抖(debounce)

![image-20211109104319394](https://www.itbaizhan.com/wiki/imgs/image-20211109104319394.png)

防抖严格算起来应该属于性能优化的知识，但实际上遇到的频率相当高，处理不当或者放任不管就容易引起浏览器卡死。

从滚动条监听的例子说起

```js
function showTop  () {
    var scrollTop = document.documentElement.scrollTop;
    console.log('滚动条位置：' + scrollTop);
}
window.onscroll  = showTop

```

在运行的时候会发现存在一个问题：这个函数的默认执行频率，太！高！了！。 高到什么程度呢？以chrome为例，我们可以点击选中一个页面的滚动条，然后点击一次键盘的【向下方向键】，会发现函数执行了8-9次！

然而实际上我们并不需要如此高频的反馈，毕竟浏览器的性能是有限的，不应该浪费在这里，所以接着讨论如何优化这种场景。

基于上述场景，首先提出第一种思路：在第一次触发事件时，不立即执行函数，而是给出一个期限值比如200ms，然后

1. 如果在200ms内没有再次触发滚动事件，那么就执行函数
2. 如果在200ms内再次触发滚动事件，那么当前的计时取消，重新开始计时

效果：如果短时间内大量触发同一事件，只会执行一次函数

实现：既然前面都提到了计时，那实现的关键就在于setTimeout这个函数，由于还需要一个变量来保存计时，考虑维护全局纯净，可以借助闭包来实现

```js
function debounce(fn,delay){
    let timer = null //借助闭包
    return function() {
        if(timer){
            clearTimeout(timer) 
        }
        timer = setTimeout(fn,delay) // 简化写法
    }
}
// 然后是旧代码
function showTop  () {
    var scrollTop = document.documentElement.scrollTop;
    console.log('滚动条位置：' + scrollTop);
}
window.onscroll = debounce(showTop,300)

```

到这里，已经把防抖实现了

> **防抖定义**
>
> 对于短时间内连续触发的事件（上面的滚动事件），防抖的含义就是让某个时间期限（如上面的1000毫秒）内，事件处理函数只执行一次

**实时效果反馈**

**1. 以下是关于定时器防抖代码，横线处填写代码是：**

```js
function debounce(fn,delay){
    let timer = null 
    return function() {
        if(timer){
            _2_(timer) 
        }
        timer = _1_(fn,delay) 
    }
}
function showTop  () {
    var scrollTop = document.documentElement.scrollTop;
    console.log('滚动条位置：' + scrollTop);
}
window.onscroll = debounce(showTop,300)

```

复制

A setTimeout clearInterval

B setTimeout clearTimeout

C setInterval clearTimeout

D setInterval clearInterval

**答案**

1=>B

## XXIV、 节流(throttle)

![image-20211109104718862](https://www.itbaizhan.com/wiki/imgs/image-20211109104718862.png)

节流严格算起来应该属于性能优化的知识，但实际上遇到的频率相当高，处理不当或者放任不管就容易引起浏览器卡死

继续思考，使用上面的防抖方案来处理问题的结果是

如果在限定时间段内，不断触发滚动事件（比如某个用户闲着无聊，按住滚动不断的拖来拖去），只要不停止触发，理论上就永远不会输出当前距离顶部的距离

但是如果产品同学的期望处理方案是：即使用户不断拖动滚动条，也能在某个时间间隔之后给出反馈呢？

其实很简单：我们可以设计一种类似控制阀门一样定期开放的函数，也就是让函数执行一次后，在某个时间段内暂时失效，过了这段时间后再重新激活（类似于技能冷却时间）

效果：如果短时间内大量触发同一事件，那么在函数执行一次之后，该函数在指定的时间期限内不再工作，直至过了这段时间才重新生效

**实现**

这里借助setTimeout来做一个简单的实现，加上一个状态位valid来表示当前函数是否处于工作状态

```js
function throttle(fn,delay){
    let valid = true
    return function() {
       if(!valid){
           //休息时间 暂不接客
           return false 
       }
       // 工作时间，执行函数并且在间隔期内把状态位设为无效
        valid = false
        setTimeout(function(){
            fn()
            valid = true;
        }, delay)
    }
}


function showTop  () {
    var scrollTop = document.documentElement.scrollTop;
    console.log('滚动条位置：' + scrollTop);
}
window.onscroll = throttle(showTop,300) 

```

如果一直拖着滚动条进行滚动，那么会以300ms的时间间隔，持续输出当前位置和顶部的距离

讲完了这两个技巧，下面介绍一下平时开发中常遇到的场景:

1. 搜索框input事件，例如要支持输入实时搜索可以使用节流方案（间隔一段时间就必须查询相关内容），或者实现输入间隔大于某个值（如500ms），就当做用户输入完成，然后开始搜索，具体使用哪种方案要看业务需求
2. 页面resize事件，常见于需要做页面适配的时候。需要根据最终呈现的页面情况进行dom渲染（这种情形一般是使用防抖，因为只需要判断最后一次的变化情况）

**实时效果反馈**

**1. 以下是关于定时器节流代码，横线处填写代码是：**

```js
function throttle(fn,delay){
    let valid = true
    return function() {
       if(_1_){
           return false 
       }
        valid = false
        _2_(function(){
            fn()
            valid = true;
        }, delay)
    }
}

```

A valid setTimeout

B valid setInterval

C !valid setTimeout

D !valid setInterval

**答案**

1=>C

# 五、jQuery

## I、关于jQuery

![image-20220108195256865](https://www.itbaizhan.com/wiki/imgs/image-20220108195256865-16577084664892.png)

现在是否还需要学习jQuery，毫无疑问到目前为止，我们仍然需要学习jQuery，原因如下：

1. 各大网站还在应用（京东、百度）
2. 一些广告页面、落地页还在应用
3. 源码非常优秀，有助于理解JavaScript
4. 其实对DOM操作并不能完全移除，只要涉及到DOM操作，jQuery是非常方便的

## II、jQuery简介



![image-20211229110658055](https://www.itbaizhan.com/wiki/imgs/image-20211229110658055.png)

jQuery 是一个高效、精简并且功能丰富的 JavaScript 工具库。它提供的 API 易于使用且兼容众多浏览器，这让诸如 HTML 文档遍历和操作、事件处理、动画操作更加简单。

jQuery最大的优点就是简化DOM操作

> 官网文档：https://jquery.com/
>
> 中文文档：https://www.jquery123.com/

### 体验jQuery

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title></title>
    <script src="./js/jquery-3.6.0.min.js" charset="utf-8"></script>
</head>
<body>
    <div class="container">
        <p class="name">Hello jQuery</p>
    </div>
    <script type="text/javascript">
        $('.name').html("Hello 体验 jQuery")
    </script>
</body>
</html>

```

### jQuery版本说明

jQuery分为三个大版本：1.x 2.x 3.x

#### 1.x版本

兼容ie678,使用最为广泛的，官方只做BUG维护，功能不再新增。因此一般项目来说，使用1.x版本就可以了，最终版本：1.12.4 (2016年5月20日)

#### 2.x版本

不兼容ie678，很少有人使用，官方只做BUG维护，功能不再新增。如果不考虑兼容低版本的浏览器可以使用2.x，最终版本：2.2.4 (2016年5月20日)

#### 3.x版本

不兼容ie678，只支持最新的浏览器。除非特殊要求，一般不会使用3.x版本的，很多老的jQuery插件不支持这个版本。目前该版本是官方主要更新维护的版本。最新版本：3.6.0

jQuery重点讲解知识点

1. 选择器
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

**实时效果反馈**

**1. 下列哪个是jQuery不能完成的事情：**

A 更便利的操作DOM

B 实现基础简单的动画效果

C 遍历元素

D jQuery链接数据库

**答案**

1=>D

##  III、选择器之基础选择器(一)

![image-20211229112906014](https://www.itbaizhan.com/wiki/imgs/image-20211229112906014.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器
      1. 类选择器
      2. 元素选择器
      3. ID选择器
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

JavaScript实现

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div class="box">类选择器</div>
    <div class="box">类选择器</div>
    <span>元素选择器</span>
    <a id="it" href="#">ID选择器</a>
    <script>
        // 类选择器
        var div1 = document.getElementsByClassName("box")[0]
        var div2 = document.getElementsByClassName("box")[1]
        div1.innerHTML = "JS类选择器1"
        div2.innerHTML = "JS类选择器2"
        // 元素选择器
        var span = document.getElementsByTagName("span")[0]
        span.innerHTML = "JS元素选择器"
        // ID选择器(ID是唯一的)
        var a = document.getElementById("it");
        a.innerHTML = "JSID选择器"
    </script>
</body>
</html>

```

jQuery实现

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div class="box">类选择器</div>
    <div class="box">类选择器</div>
    <span>元素选择器</span>
    <a id="it" href="#">ID选择器</a>
    <script>
        // $就是jQuery的缩写，他就代表了jQuery
        // 类选择器
        $(".box").html("jQuery类选择器")
        // 元素选择器
        $("span").html("jQuery元素选择器")
        // ID选择器
        $("#it").html("jQuery ID选择器")
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个选择器具有唯一性，不可以同时选中多个元素：**

A 类选择器

B 元素选择器

C ID选择器

D 通用选择器

**答案**

1=>C

##  IV、选择器之基础选择器(二)

![image-20211229113045986](https://www.itbaizhan.com/wiki/imgs/image-20211229113045986.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器
      1. 类选择器
      2. 元素选择器
      3. ID选择器
      4. 子元素选择器
      5. 后代元素选择器
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### 子元素选择器 ("parent > child")

选择所有指定“parent”元素中指定的"child"的直接子元素

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            font-size: 14px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <ul class="topnav">
        <li>Item 1</li>
        <li>Item 2
            <ul>
                <li>child item 1</li>
                <li>child item 2</li>
                <li>child item 3</li>
            </ul>
        </li>
        <li>Item 3</li>
    </ul>
    <script>
        $(".topnav > li").css("border", "3px double red");
    </script>
</body>
</html>

```

### 后代元素选择器（"parent child"）

选择所有指定“parent”元素中指定的"child"的后代元素

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            font-size: 14px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <ul class="topnav">
        <li>Item 1</li>
        <li>Item 2
            <ul>
                <li>child item 1</li>
                <li>child item 2</li>
                <li>child item 3</li>
            </ul>
        </li>
        <li>Item 3</li>
    </ul>
    <script>
        $(".topnav li").css("border", "3px double red");
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 子选择器和后代选择器的区别下列描述错误的是：**

A 子选择器选择所有“parent”元素中的"child"的直接子元素

B 后代选择器选择所有“parent”元素中的"child"的后代元素

C 子选择器与后代选择器一样，没有区别

D 子选择器与后代选择器选择的范围不同

**答案**

1=>C

##  V、选择器之属性选择器(一)

![image-20211229115254126](https://www.itbaizhan.com/wiki/imgs/image-20211229115254126.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器
      1. 类选择器
      2. 元素选择器
      3. ID选择器
      4. 子元素选择器
      5. 后代元素选择器
   2. 属性选择器
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

属性选择器有很多操作方式（6个）

### Attribute Selector [name="value"]

选择指定属性是给定值的元素

> attribute: 属性
>
> Selector: 选择器
>
> name: 选中的属性
>
> value: 属性值

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div>
        <input type="radio" name="user" value="name" />
        <span>name</span>
    </div>
    <div>
        <input type="radio" name="user" value="age" />
        <span>age</span>
    </div>
    <script>
        $('input[value="name"]').next().html("username");
    </script>
</body>
</html>

```



### Attribute Selector [name|="value"]

选择指定属性值等于给定字符串或以该字符串为前缀（该字符串后跟一个连字符“-” ）的元素

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <a href="#" alt="sxt">尚学堂</a>
    <a href="#" alt="sxt-web">尚学堂-前端</a>
    <a href="#" alt="sxtitbaizhan">itbaizhan</a>
    <script>
        $('a[alt|="sxt"]').css('border', '3px solid green');
    </script>
</body>
</html>

```

### Attribute Selector [name*="value"]

选择指定属性具有包含一个给定的子字符串的元素。（选择给定的属性是以包含某些值的元素）

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input name="sxt-itbaizhan" />   
    <input name="sxtweb" />
    <input name="bjsxtweb" />
    <input name="itbaizhan" />
    <script>$('input[name*="sxt"]').val('study!');</script>
</body>
</html>

```

**实时效果反馈**

**1. 下列关于属性选择器，哪个是选中包含给定字符串元素的选择器：**

A Attribute Selector [name="value"]

B Attribute Selector [name|="value"]

C Attribute Selector [name*="value"]

**答案**

1=>B

##  VI、选择器之属性选择器(二)

![image-20211229115254126](https://www.itbaizhan.com/wiki/imgs/image-20211229115254126.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器
      1. 类选择器
      2. 元素选择器
      3. ID选择器
      4. 子元素选择器
      5. 后代元素选择器
   2. 属性选择器
      1. 完美匹配
      2. 包含
      3. 前缀
      4. 开头
      5. 结尾
      6. 空格
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### Attribute Selector [name~="value"]

选择指定属性用空格分隔的值中包含一个给定值的元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input type="text" name="sxt-itbaizhan">
    <input type="text" name="sxt web">
    <input type="text" name="bjsxtweb">
    <script>
        // 属性选择器：空格隔开的独立的单词可以匹配 匹配sxt
        $("input[name ~= 'sxt']").css("border","2px solid red")
    </script>
</body>
</html>
```

### Attribute Selector [name$="value"]

选择指定属性是以给定值结尾的元素。这个比较是区分大小写的

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input  name="sxt-itbaizhan">
    <input  name="sxt web">
    <input  name="bjsxtweb">
    <script>
        // 属性选择器：匹配给定结尾的字符串 咱们匹配web
        $("input[name $= 'web']").css("border","2px solid green")
    </script>
</body>
</html>
```

### Attribute Selector [name^="value"]

选择指定属性是以给定字符串开始的元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input type="text" name="sxt-itbaizhan">
    <input type="text" name="sxt web">
    <input type="text" name="bjsxtweb">
    <script>    
    // 属性选择器：匹配开头元素 匹配sxt
        $("input[name ^= 'sxt']").css("border","2px solid red")
    </script>
</body>
</html>
```

**实时效果反馈**

**1. 下列关于属性选择器，哪个是选中给定字符串开始的元素选择器：**

A Attribute Selector [name~="value"]

B Attribute Selector [name$="value"]

C Attribute Selector [name^="value"]

**答案**

1=>C

## VII、选择器之jQuery扩展(一)

![image-20211229120630896](https://www.itbaizhan.com/wiki/imgs/image-20211229120630896.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器
      1. 类选择器
      2. 元素选择器
      3. ID选择器
      4. 子元素选择器
      5. 后代元素选择器
   2. 属性选择器
      1. 完美匹配
      2. 包含
      3. 前缀
      4. 开头
      5. 结尾
      6. 空格
   3. jQuery选择器
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### :eq(index) Selector

在匹配的集合中选择索引值为index的元素。

> **温馨提示**
>
> index下标计算是从0开始的

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <ul>
        <li>item 1</li>
        <li>item 2</li>
        <li>item 3</li>
        <li>item 4</li>
        <li>item 5</li>
        <li>item 6</li>
    </ul>
    <script>
        // jquery 扩展选择器： :eq(index)   index:下标从0开始  选中第三个li标签
        $("li:eq(2)").css("border","2px solid red")
    </script>
</body>
</html>
```

### :even Selector

选择所引值为偶数的元素

> **特别注意**
>
> 这是基于0的索引，所以`:even`选择器是选择第一个元素，第三个元素，依此类推在匹配。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <table border="1">
        <tr>
            <td>Row with Index #0</td>
        </tr>  <!-- 0-->
        <tr>
            <td>Row with Index #1</td>
        </tr> <!-- 1-->

        <tr>
            <td>Row with Index #2</td>
        </tr> <!-- 2-->
        <tr>
            <td>Row with Index #3</td>
        </tr> <!-- 3-->
    </table>
    <script>
        // jquery 扩展选择器：even偶数选择器 注意：从0开始
        $("tr:even").css("background-color","red")
    </script>
</body>
</html>
```



### :odd Selector

选择索引值为奇数元素

> **特别注意**
>
> 这是基于0的索引，所以`:odd`选择器是选择第二个元素，第四个元素，依此类推在匹配。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <table border="1">
        <tr>
            <td>Row with Index #0</td>
        </tr>  <!-- 0-->
        <tr>
            <td>Row with Index #1</td>
        </tr> <!-- 1-->

        <tr>
            <td>Row with Index #2</td>
        </tr> <!-- 2-->
        <tr>
            <td>Row with Index #3</td>
        </tr> <!-- 3-->
    </table>
    <script>
        // jquery 扩展选择器：odd奇数选择器 注意：从0开始
        $("tr:odd").css("background-color","red")
    </script>
</body>
</html>
```

**实时效果反馈**

**1. 下列jQuery扩展选择器中,哪个是通过`index`下标选择某个元素：**

A :eq(index) Selector

B :even Selector

C :odd Selector

**答案**

1=>A

##  VIII、选择器之jQuery扩展(二)

![image-20211229120630896](https://www.itbaizhan.com/wiki/imgs/image-20211229120630896.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### :first Selector

选择第一个匹配的元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <table border="1">
        <tr>
            <td>Row 1</td>
        </tr>
        <tr>
            <td>Row 2</td>
        </tr>
        <tr>
            <td>Row 3</td>
        </tr>
    </table>
    <script>
        // jQuery扩展选择器：first第一个元素选择器
        $("td:first").css("background-color","red")
    </script>
</body>
</html>
```

### :last Selector

选择最后一个匹配的元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <table border="1">
        <tr>
            <td>Row 1</td>
        </tr>
        <tr>
            <td>Row 2</td>
        </tr>
        <tr>
            <td>Row 3</td>
        </tr>
    </table>
    <script>
        // jQuery扩展选择器：last最后一个元素选择器
        $("td:last").css("background-color","red")
    </script>
</body>
</html>
```

### :gt(index) Selector

选择匹配集合中所有大于给定index（索引值）的元素。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <table border="1">
        <tr>
            <td>TD #0</td>
            <td>TD #1</td>
            <td>TD #2</td>
        </tr>
        <tr>
            <td>TD #3</td>
            <td>TD #4</td>
            <td>TD #5</td>
        </tr>
        <tr>
            <td>TD #6</td>
            <td>TD #7</td>
            <td>TD #8</td>
        </tr>
    </table>
    <script>
        // jQuery扩展选择器：gt(index) 大于index的值
        $("td:gt(5)").css("background-color","red")
    </script>
</body>
</html>
```

### :lt(index) Selector

选择匹配集合中所有索引值小于给定index参数的元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <table border="1">
        <tr>
            <td>TD #0</td>
            <td>TD #1</td>
            <td>TD #2</td>
        </tr>
        <tr>
            <td>TD #3</td>
            <td>TD #4</td>
            <td>TD #5</td>
        </tr>
        <tr>
            <td>TD #6</td>
            <td>TD #7</td>
            <td>TD #8</td>
        </tr>
    </table>
    <script>
        // jQuery扩展选择器：lt(index) 小于于index的值
        $("td:lt(5)").css("background-color","red")
    </script>
</body>
</html>
```



**实时效果反馈**

**1. 下列jQuery扩展选择器中,哪个是通过`index`下标选择某一个元素：**

A :eq(index) Selector

B :even Selector :odd Selector

C :first Selector :last Selector

D :gt(index) Selector :lt(index) Selector

**答案**

1=>A

##  IX、DOM操作(一)

![image-20211229135940824](https://www.itbaizhan.com/wiki/imgs/image-20211229135940824.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. addClass()
   2. removeClass()
   3. toggleClass()
   4. hasClass()
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### addClass()

给元素添加class，值得注意的是这个方法不会替换一个样式类名。它只是简单的添加一个样式类名到元素上

```js
$("p").addClass("myClass");
```

也可以同时添加多个class

```javascript
$("p").addClass("myClass1 myClass2");
```

### removeClass()

移除元素中每个匹配元素上一个，多个或全部样式

通过class名字移除元素

```js
$('p').removeClass('myClass yourClass')
```

移除全部class

```js
 $('p').removeClass()
```

配合addClass() 一起使用用来切换元素的样式

```js
 $('p').removeClass('myClass noClass').addClass('yourClass');
```

### toggleClass()

这是一个开关方法，如果class存在则删除，如果class不存在则添加

```js
 $('#foo').toggleClass(className, addOrRemove);
```

### hasClass()

判断一个元素上是否具有某个class

```js
<!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>gt demo</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div id="mydiv" class="foo bar"></div>
    <script>
        var flag = $('#mydiv').hasClass('foo')
        if(flag){
            $('#mydiv').html("div具有foo class")
        }
    </script>
</body>
</html>

```

**综合**：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div class="error">Hello</div>
    <span class="txt">Hello</span>
    <a href="#" class="active"></a>
    <img src="" alt="" class="img">
    <script>
        /**
         * 1、addClass()：添加Class，不会覆盖原有的class，可以添加多个class，用空格隔开
         * 2、removeClass()：移除class，可以移除一个或者多个，也可以全部移除
         * 3、toggleClass()：开关，如果存在则删除，如果不存在则添加
         * 4、hasClass()：判断一个元素是否存在某个class，存在返回true,不存在返回false
         * 
         * 补充知识点：在jQuery中,有个链式调用
         * */
        $("div").addClass("txt success")
        $("div").removeClass("txt error")
        $("div").toggleClass("txt")

        var flag = $("a").hasClass("active")
        console.log(flag);
        if(flag){
            console.log("a标签存在active");
        }else{
            console.log("a标签不存在active");
        }

        // 给某个元素添加一个class然后再移除一个class
        // 把img的class="img"移除掉，再添加个class="image"
        // $("img").addClass("image")
        // $("img").removeClass("img")
        $("img").removeClass("img").addClass("image") // 链式调用
    </script>
</body>
</html>
```

**实时效果反馈**

**1. jQuery针对元素class的操作,下列哪个是判断一个元素是否存在的方法：**

A addClass()

B removeClass()

C toggleClass()

D hasClass()

**答案**

1=>D

##  X、DOM操作(二)

![image-20211229140855816](https://www.itbaizhan.com/wiki/imgs/image-20211229140855816.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. addClass()
   2. removeClass()
   3. toggleClass()
   4. hasClass()
   5. html()
   6. text()
   7. val()
   8. attr()
   9. removeAttr()
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### html()

获取元素中的HTML内容

```html
$('div.demo-container').html();
```

html()方法还可以设置元素的html内容

```html
$('div.demo-container').html('<p>All new content. <em>You bet!</em></p>');
```

### val()

用于获取`<input>`标签中的内容

```html
$(".input").val();
```

也可以设置`<input>`标签内容

```html
$(".input").val("username")
```

### attr()

获取匹配的元素的属性的值 或 设置匹配元素的一个或多个属性

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        img {
            padding: 10px;
            width: 100px;
        }
        div {
            color: red;
            font-size: 24px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <img />
    <div><B>Attribute of Ajax</B></div>
    <script>
        $("img").attr({
            src: "images/1.jpeg",
            title: "jQuery",
            alt: "jQuery Logo"
        });
        $("div").text($("img").attr("alt"));
    </script>
</body>
</html>

```

### removeAttr()

为匹配的元素集合中的每个元素中移除一个属性（attribute）

```html
img.removeAttr("title")
```

**实时效果反馈**

**1. 下列关于jQuery的DOM操作,哪个方法可以设置元素属性：**

A html()

B val()

C attr()

D removeAttr()

**答案**

1=>C

##  XI、DOM操作(三)

![image-20211229141055622](https://www.itbaizhan.com/wiki/imgs/image-20211229141055622.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容
      1. .wrap()
      2. .unwrap()
      3. .wrapAll()
      4. .wrapInner()
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### DOM 插入并包裹现有内容

#### .wrap()

在每个匹配的元素外层包上一个html元素

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>itbaizhan</p>
    <script>
        $("p").wrap("<div class='container'></div>");
    </script>
</body>
</html>

```

#### .unwrap()

将匹配元素集合的父级元素删除，保留自身在原来的位置

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div>
        <p>itbaizhan</p>
    </div>
    <script>
        $("p").unwrap();
    </script>
</body>
</html>

```

#### .wrapAll()

在所有匹配元素外面包一层HTML结构

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    div { border: 2px solid blue; }
    p { background:yellow; margin:4px; }
  </style>
  <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>itbaizhan</p>
    <p>sxt</p>
    <p>web</p>
    <script>
        $("p").wrapAll("<div></div>");
    </script>
</body>

```

#### .wrapInner()

在匹配元素里的内容外包一层结构

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        p {
            background: #bbf;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>itbaizhan</p>
    <p>sxt</p>
    <p>web</p>
    <script>$("p").wrapInner("<b></b>");</script>
</body>
</html>

```

**实时效果反馈**

**1. DOM插入操作,如何在所有同级元素外增加一个容器,选择下列哪个方法：**

A wrap()

B unwrap()

C wrapAll()

D wrapInner()

**答案**

1=>C

##  XII、DOM操作(四)

![image-20211229142530942](https://www.itbaizhan.com/wiki/imgs/image-20211229142530942.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内
      1. .append()
      2. .prepend()
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### DOM 插入现有元素内

在一个现有元素内插入新内容

#### .append()

在每个匹配元素里面的末尾处插入参数内容

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>I would like to say: </p>
    <script>
        $("p").append("<strong>Hello</strong>");
    </script>
</body>
</html>

```

#### .prepend()

将参数内容插入到每个匹配元素的前面（元素内部）

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>, itbaizhan</p>
    <script>
        $("p").prepend("<strong>Hello</strong>");
    </script>
</body>
</html>

```

**实时效果反馈**

**1. DOM插入操作,如何在一个元素里面尾部插入数据：**

A append()

B prepend()

C wrapAll()

D wrapInner()

**答案**

1=>A

## XIII、 DOM操作(五)

![image-20211229143410050](https://www.itbaizhan.com/wiki/imgs/image-20211229143410050.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外
      1. .after()
      2. .before()
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### DOM 插入现有元素外

在一个现有元素外插入新内容

#### .after()

在匹配元素集合中的每个元素后面插入参数所指定的内容，作为其兄弟节点

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>I would like to say: </p>
    <script>$("p").after("<b>Hello</b>");</script>
</body>
</html>

```

#### .before()

根据参数设定，在匹配元素的前面插入内容，作为其兄弟节点

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>I would like to say: </p>
    <script>$("p").before("<b>Hello</b>");</script>
</body>
</html>

```

**实时效果反馈**

**1. DOM插入操作,如何在一个元素同级后面插入新的元素：**

A append()

B prepend()

C after()

D before()

**答案**

1=>C

##  XIV、DOM操作(六)

![image-20211229143853637](https://www.itbaizhan.com/wiki/imgs/image-20211229143853637.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除
      1. .empty()
      2. .remove()
   8. DOM 替换
      1. .replaceAll()
      2. .replaceWith()
3. CSS操作
4. 事件处理
5. 遍历
6. 动画

### DOM 移除

从 DOM 树中删除元素

#### .empty()

从DOM中移除集合中匹配元素的所有子节点

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>
        Hello, <span>Person</span> <a href="javascript:;">and person</a>
    </p>
    <script>
        $("p").empty();
    </script>
</body>
</html>

```

#### .remove()

将匹配元素集合从DOM中删除

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>Hello</p>
    <script>
        $("p").remove();
    </script>
</body>

```

### DOM 替换

从 DOM 树中移除已有的内容并将其替换为新内容

#### .replaceAll()

用集合的匹配元素替换每个目标元素

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>Hello</p>
    <script>
        $("<b>World</b>").replaceAll("p");
    </script>
</body>
</html>

```

#### .replaceWith()

用提供的内容替换集合中所有匹配的元素

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>Wrold</p>
    <script>
        $("p").replaceWith("<div>Hello</div>");
    </script>
</body>
</html>

```

**实时效果反馈**

**1. DOM操作中,如何把一个容器中的内容全部删除：**

A empty()

B remove()

C replaceAll()

D replaceWith()

**答案**

1=>A

##  XV、CSS操作(一)

![image-20211229154630270](https://www.itbaizhan.com/wiki/imgs/image-20211229154630270.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. .css()
   2. .height()，.width()
   3. .innerHeight()，.innerWidth()
   4. .outerHeight()，.outerWidth()
4. 事件处理
5. 遍历
6. 动画

### .css()

获取和设置匹配元素的样式

#### 获取样式值

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        div {
            width: 60px;
            height: 60px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div style="background-color:#123456;">div容器</div>
    <script>
        var color = $("div").css("background-color");
        console.log(color);
    </script>
</body>
</html>

```

#### 设置样式

```html
<!DOCTYPE html>
<html>
<head>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p>Hello,itbaizhan</p>
    <script>
        $("p").css("color", "red");
    </script>
</body>
</html>

```

### .height()，.width()

获取元素的当前高度值宽度值或设置元素的高度值宽度值

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        div {
            width: 100px;
            height: 100px;
            margin: 5px;
            background: rgb(255, 140, 0);
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div></div>
    <script>
        $("div").height(200).width(200)
    </script>
</body>
</html>

```

### .innerHeight()，.innerWidth()

为元素的当前计算高度值和宽度值,包括padding，但是不包括border

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        div {
            width: 100px;
            height: 100px;
            padding: 10px;
            border: 5px solid red;
            margin: 10px;
            background: rgb(255, 140, 0);
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div></div>
    <script>
        var currentHeight = $("div").innerHeight();
        var currentWidth = $("div").innerWidth();
        console.log(currentHeight,currentWidth);
    </script>
</body>
</html>

```

### .outerHeight()，.outerWidth()

获取元素的当前宽度值和高度值,包括padding，border和选择性的margin

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        div{
            width: 100px;
            height: 100px;
            margin: 10px;
            padding: 5px;
            border: 10px solid #666;
            background-color: red;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div></div>
    <p class="text2"></p>
    <script>
        $(".text2").text("outerWidth:" + $("div").outerWidth() + " , outerWidth(true):" + $("div").outerWidth(true));
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个属性是获取一个元素的大小,包括padding，但是不包括border：**

A height() , width()

B innerHeight() , innerWidth()

C outerHeight() , outerWidth()

**答案**

1=>B

##  XVI、CSS操作(二)

![image-20211229155029902](https://www.itbaizhan.com/wiki/imgs/image-20211229155029902.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置
      1. .offset()
      2. .position()
      3. .scrollLeft(), .scrollTop()
4. 事件处理
5. 遍历
6. 动画

### .offset()

获取元素的当前坐标，或设置每一个元素的坐标，坐标相对于文档

#### 获取位置

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        p {
            margin: 10px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <p class="text1">Hello</p>
    <p class="text2"></p>
    <script>
        var offset = $(".text1").offset();
        $(".text2").html("left: " + offset.left + ", top: " + offset.top);
    </script>
</body>
</html>

```

#### 设置位置

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        div {
            width: 100px;
            height: 100px;
            background-color: red;
            position: relative;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div></div>
    <script>
        $("div").offset({ top: 100, left: 100 });
    </script>
</body>
</html>

```

### .position()

获取元素的当前坐标，相对于`offset parent`的坐标

> **温馨提示**
>
> `.position()`方法可以取得元素相对于父元素的偏移位置。与`.offset()`不同, `.offset()`是获得该元素相对于`documet`的当前坐标 当把一个新元素放在同一个容器里面另一个元素附近时，用`.position()`更好用。

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .container{
            width: 300px;
            height: 200px;
            border: 2px solid #000;
            margin-left: 100px;
            position: relative;
        }
        .box {
            width: 100px;
            height: 100px;
            padding: 15px;
            background-color: red;
            position: absolute;
            left: 10px;
            top: 10px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div class="container">
        <div class="box"></div>
    </div>
    <p class="text1"></p>
    <p class="text2"></p>
    <script>
        var position = $(".box").position();
        var offset = $(".box").offset();
        $(".text1").text("left: " + position.left + ", top: " + position.top);
        $(".text2").text("left: " + offset.left + ", top: " + offset.top);
    </script>
</body>
</html>

```

### .scrollLeft(), .scrollTop()

获取元素的当前水平和垂直滚动条的位置。设置每个匹配元素的水平和垂直滚动条位置

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        .container {
            background: #CCCCCC;
            border: 3px solid #666666;
            margin: 5px;
            padding: 5px;
            width: 200px;
            height: 200px;
            overflow: auto;
        }
        p {
            margin: 10px;
            padding: 5px;
            border: 2px solid #666;
            width: 1000px;
            height: 1000px;
        }
    </style>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div class="container">
        <h1>itbaizhan</h1>
        <p>sxt</p>
    </div>
    <span class="text"></span>
    <script>
        $(".container").scrollLeft(300);
        var scrollLeft = $(".container").scrollLeft();
        console.log(scrollLeft);
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 获取一个元素相对于父级元素的位置偏移,使用下列哪个属性：**

A offset()

B position()

C scrollLeft()

D scrollTop()

**答案**

1=>B

 事件之绑定事件处理器

![image-20211229160036071](https://www.itbaizhan.com/wiki/imgs/image-20211229160036071.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. .on()
   2. .one()
   3. .off()
5. 遍历
6. 动画

### .on()

在选定的元素上绑定一个或多个事件处理函数

```html
$("#button").on("click", function(event){
    console.log("事件处理器")
});

```

事件委托

```html
$("#ul").on("click", "li", function(event){
  console.log($(this).text());
});

```

### .one()

为元素的事件添加处理函数。处理函数在每个元素上每种事件类型最多执行一次

```html
$("#btn").one("click", function() {
  console.log("这是一个只能触发一次的事件.");
});

```

### .off()

移除一个事件处理函数，移除on事件处理器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <button id="btn1">添加事件按钮</button>
    <button id="btn2">删除事件按钮</button>
    <button id="btn3">按钮</button>
    <script>
        function aClick() {
            console.log("点击事件")
        }
        $("#btn1").on("click",function () {
            $("#btn3").on("click", aClick);
        });
        $("#btn2").on("click",function () {
            $("#btn3").off("click", aClick);
        });
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个事件处理程序,可以完成事件委托：**

A on()

B one()

C off()

D click()

**答案**

1=>A

## XVII、事件之绑定事件处理器

![image-20211229160036071](https://www.itbaizhan.com/wiki/imgs/image-20211229160036071.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. .on()
   2. .one()
   3. .off()
5. 遍历
6. 动画

### .on()

在选定的元素上绑定一个或多个事件处理函数

```html
$("#button").on("click", function(event){
    console.log("事件处理器")
});

```

事件委托

```html
$("#ul").on("click", "li", function(event){
  console.log($(this).text());
});

```

### .one()

为元素的事件添加处理函数。处理函数在每个元素上每种事件类型最多执行一次

```html
$("#btn").one("click", function() {
  console.log("这是一个只能触发一次的事件.");
});

```

### .off()

移除一个事件处理函数，移除on事件处理器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <button id="btn1">添加事件按钮</button>
    <button id="btn2">删除事件按钮</button>
    <button id="btn3">按钮</button>
    <script>
        function aClick() {
            console.log("点击事件")
        }
        $("#btn1").on("click",function () {
            $("#btn3").on("click", aClick);
        });
        $("#btn2").on("click",function () {
            $("#btn3").off("click", aClick);
        });
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个事件处理程序,可以完成事件委托：**

A on()

B one()

C off()

D click()

**答案**

1=>A

 

##  XVIII、事件之鼠标事件

![image-20211229164626650](https://www.itbaizhan.com/wiki/imgs/image-20211229164626650.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件
      1. .click()
      2. .hover()
      3. .mouseenter()
      4. .mouseleave()
      5. .mousemove()
      6. .mouseover()
      7. .mouseout()
5. 遍历
6. 动画

### .click()

为 JavaScript 的"click" 事件绑定一个处理器，或者触发元素上的 "click" 事件

```html
$("#btn").click(function() {
  alert("点击事件");
});

```

### .hover()

将二个事件函数绑定到匹配元素上，分别当鼠标指针进入和离开元素时被执行

```html
$("li").hover(
  // 滑入
  function () {
    console.log("滑入")
  },
  // 滑出
  function () {
    console.log("滑出")
  }
);

```



### .mouseenter()

鼠标进入事件

```html
$("div").mouseenter(function(){
    console.log("鼠标进入事件");
})

```

### .mouseleave()

鼠标离开事件

```html
$("div").mouseleave(function(){
    console.log("鼠标进入事件");
})

```

### .mousemove()

鼠标滑动事件

```html
$("div").mousemove(function(){
    console.log("鼠标进入事件");
})

```

### .mouseover()

鼠标进入事件（注：支持事件冒泡）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
    <style>
        .container{
            width: 200px;
            height: 200px;
            background-color: red;
        }
        .box{
            width: 100px;
            height: 100px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="box"></div>
    </div>
    <script>
        $(".container").mouseover(function(){
            console.log("鼠标进入事件container");
        })
        $(".box").mouseover(function(){
            console.log("鼠标进入事件box");
        })


    </script>
</body>
</html>

```

### .mouseout()

鼠标离开事件（注：支持事件冒泡）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
    <style>
        .container{
            width: 200px;
            height: 200px;
            background-color: red;
        }
        .box{
            width: 100px;
            height: 100px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="box"></div>
    </div>
    <script>
        $(".container").mouseout(function(){
            console.log("鼠标离开事件container");
        })
        $(".box").mouseout(function(){
            console.log("鼠标离开事件box");
        })
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个事件可以完成鼠标进入与滑出的监听：**

A click()

B hover()

C mouseenter()

D mouseleave()

**答案**

1=>B

##  XIX、事件之表单事件

![image-20211229171911251](https://www.itbaizhan.com/wiki/imgs/image-20211229171911251.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件
      1. .focus()
      2. .blur()
      3. .change()
      4. .submit()
5. 遍历
6. 动画

### .focus()

为 JavaScript 的 "focus" 事件绑定一个获取焦点处理函数，或者触发元素上的 "focus" 事件

```html
$('#input').focus(function() {
  alert('获得焦点事件');
});

```

### .blur()

为 "blur" 事件绑定一个失去焦点处理函数

```html
$('#other').click(function() {
  $('#target').blur();
});

```



### .change()

为JavaScript 的 "change" 事件绑定一个表单改变处理函数

```html
$('.target').change(function() {
  alert('内容改变');
});

```

### .submit()

当用户提交表单时，就会在这个表单元素上触发submit事件。它只能绑定在`<form>`元素上

```html
$('#target').submit(function() {
  alert('表单提交事件');
});

```

**实时效果反馈**

**1. 下列哪个方法是获取到焦点的事件：**

A focus()

B blur()

C change()

D submit()

**答案**

1=>A

##  XX、事件之键盘事件

![image-20211229172702037](https://www.itbaizhan.com/wiki/imgs/image-20211229172702037.png)

 

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件 .focus() .blur() .change() .submit()
   4. 键盘事件 .keydown() .keypress() .keyup()
5. 遍历
6. 动画

### .keydown()

添加键盘按下事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input type="text" class="username">
    <script>
        $(".username").keydown(function(){
            console.log("键盘");
        })
    </script>
</body>
</html>

```

### .keypress()

添加键盘事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input type="text" class="username">
    <script>
        $(".username").keypress(function(){
            console.log("键盘");
        })
    </script>
</body>
</html>

```



### .keyup()

添加键盘抬起事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <input type="text" class="username">
    <script>
        $(".username").keyup(function(){
            console.log("键盘");
        })
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个是键盘按键抬起触发的事件：**

A keydown()

B keypress()

C keyup()

D click()

**答案**

1=>C

##  XXI、事件之浏览器事件

![image-20211229180921625?v=1.0.1](https://www.itbaizhan.com/wiki/imgs/image-20211229180921625.png?v=1.0.1)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件 .focus() .blur() .change() .submit()
   4. 键盘事件 .keydown() .keypress() .keyup()
   5. 浏览器事件
      1. .resize()
      2. .scroll()
5. 遍历
6. 动画

### .resize()

添加浏览器窗口发生变化触发事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <script>
        $(window).resize(function(){
            console.log("改变浏览器尺寸");
        })
    </script>
</body>
</html>

```

### .scroll()

浏览器滚动事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <script>
        $(window).scroll(function(){
            console.log("滚动");
        })
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个是浏览器滚动事件：**

A resize()

B scroll()

C change()

D click()

**答案**

1=>B

##  XXII、事件对象

![image-20211230104752376](https://www.itbaizhan.com/wiki/imgs/image-20211230104752376.png?v=1.0.0)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件 .focus() .blur() .change() .submit()
   4. 键盘事件 .keydown() .keypress() .keyup()
   5. 浏览器事件 .resize() .scroll()
   6. 事件对象 event.type event.target event.currentTarget event.preventDefault() event.stopPropagation()
5. 遍历
6. 动画

### event.type

获取事件类型

```html
$("#btn").click("click",function(e){
    console.log(e.type);
})

```

### event.target

获取当前元素对象

```html
$("#btn").click("click",function(e){
    console.log(e.target);
})

```

### event.currentTarget

获取当前元素对象

> **温馨提示**
>
> target：指向触发事件元素
>
> currentTarget：指向添加事件的元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div id="container">
        <button id="btn">按钮</button>
    </div>
    <script>
        $("#container").click("click",function(e){
            console.log("container",e.currentTarget);
            console.log("container",e.target);
        })
        $("#btn").click("click",function(e){
            console.log("btn",e.currentTarget);
            console.log("btn",e.target);
        })
    </script>
</body>
</html>

```

### event.preventDefault()

如果调用这个方法，默认事件行为将不再触发。

```html
<a href="https://itbaizhan.com">itbaizhan</a>
<script>
    $("a").click("click",function(e){
        e.preventDefault();
    })
</script>

```

### event.stopPropagation()

防止事件冒泡到DOM树上，也就是不触发的任何前辈元素上的事件处理函数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div>
        <button>按钮</button>
    </div>
    <script>
        $("div").click("click",function(e){
            console.log("div");
        })
        $("button").click("click",function(e){
            e.stopPropagation();
            console.log("button");
        })
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列关于事件对象，哪个是阻止事件冒泡的方法：**

A target()

B currentTarget()

C preventDefault()

D stopPropagation()

**答案**

1=>D

##  XXIII、jQuery遍历

![image-20211230110850812?v=1.0.1](https://www.itbaizhan.com/wiki/imgs/image-20211230110850812.png?v=1.0.1)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件 .focus() .blur() .change() .submit()
   4. 键盘事件 .keydown() .keypress() .keyup()
   5. 浏览器事件 .resize() .scroll()
   6. 事件对象 event.type event.target event.currentTarget event.preventDefault() event.stopPropagation()
5. 遍历
   1. 列表遍历 .map() .each()
   2. 列表中获得一个JS对象的DOM元素 .get()
6. 动画

### .map()

通过一个函数匹配当前集合中的每个元素,产生一个包含新的jQuery对象

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>


    <ul>
        <li>列表1</li>
        <li>列表2</li>
        <li>列表3</li>
        <li>列表4</li>
    </ul>
   
    <script>
        $("li").map(function(index,ele){
            console.log(index,ele);
        })
    </script>
</body>
</html>

```

### .each()

遍历一个jQuery对象，为每个匹配元素执行一个函数

```html
$("li").each(function(index,ele){
    console.log(index,ele);
})

```

> **温馨提示**
>
> each和map的返回值不同，map返回一个新的数组，each返回原始数组

### .get()

通过jQuery对象获取一个对应的DOM元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <ul>
        <li>列表1</li>
        <li>列表2</li>
        <li>列表3</li>
        <li>列表4</li>
    </ul>
    <script>
        var li = $("li").get(0);
        li.innerHTML = "新的列表"
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个方法不可以把一个jQuery对象转换成一个JS对象：**

A map()

B each()

C get()

D target()

**答案**

1=>C

##  XXIV、jQuery树遍历

![image-20220112142654984](https://www.itbaizhan.com/wiki/imgs/image-20220112142654984.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件 .focus() .blur() .change() .submit()
   4. 键盘事件 .keydown() .keypress() .keyup()
   5. 浏览器事件 .resize() .scroll()
   6. 事件对象 event.type event.target event.currentTarget event.preventDefault() event.stopPropagation()
5. 遍历
   1. 列表遍历 .map() .each()
   2. 列表中获得一个JS对象的DOM元素 .get()
   3. 树遍历（关系）
      1. .children()
      2. .find()
      3. .next()
      4. .parent()
      5. .siblings()
6. 动画

### .children()

获得子元素，可以传递一个选择器参数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <ul class="first">
        <li>item 1</li>
        <li>
            <ul class="secode">
                <li>child item 1</li>
                <li>child item 2</li>
                <span>child span</span>
            </ul>
        </li>
        <li>item 3</li>
    </ul>
    <script>
        $(".first").children().css("border","1px solid red")
        $(".first").children("li").css("border","1px solid red")
    </script>
</body>
</html>

```

### .find()

寻找后代元素

> **温馨提示**
>
> `.find()`和`.children()`方法是相似的，但后者只是再DOM树中向下遍历一个层级（注：就是只查找子元素，而不是后代元素）。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <ul class="first">
        <li>item 1</li>
        <li>
            <ul class="secode">
                <li>child item 1</li>
                <li>child item 2</li>
                <span>child span</span>
            </ul>
        </li>
        <li>item 3</li>
    </ul>
    <script>
        $(".first").find("li").css("border","1px solid red")
    </script>
</body>
</html>

```

### .next()

取得元素紧邻的后面同辈元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div>Hello</div>
    <p>内容</p>
    <span>元素</span>
    <script>
        $("div").next().css("border","2px solid red")
    </script>
</body>
</html>

```

### .parent()

取得元素的父元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div>
        <p>Hello</p>
    </div>
    <script>
       $("p").parent().css("border","2px solid red")
    </script>
</body>
</html>

```

### .siblings()

获得元素的兄弟元素，可以传递一个选择器参数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div>
        <p>Hello1</p>
        <p>Hello2</p>
        <span>World</span>
        <p class="text">Hello3</p>
        <p>Hello4</p>
        <p>Hello5</p>
    </div>
    <script>
       $(".text").siblings().css("border","2px solid red")
       $(".text").siblings("p").css("border","2px solid red")
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
</head>
<body>
    <div>
        <p>Hello1</p>
        <p>Hello2</p>
        <span>World</span>
        <p class="text">Hello3</p>
        <p>Hello4</p>
        <p>Hello5</p>
    </div>
    <script>
       $(".text").siblings().css("border","2px solid red")
       $(".text").siblings("p").css("border","2px solid red")
    </script>
</body>
</html>

```

**实时效果反馈**

**1. 下列哪个方法可以获得元素同级关系：**

A children()

B find()

C next()

D siblings()

**答案**

1=>D

## XXV、jQuery动画(一)

![image-20211230115931351](https://www.itbaizhan.com/wiki/imgs/image-20211230115931351.png)

### jQuery重点讲解知识点

1. 选择器
   1. 基础选择器 类选择器 元素选择器 ID选择器 子元素选择器 后代元素选择器
   2. 属性选择器 完美匹配 包含 前缀 开头 结尾 空格
   3. jQuery扩展选择器 eq even odd first last gt lt
2. DOM操作
   1. Class操作 addClass() removeClass() toggleClass() hasClass()
   2. 文本操作 html() text() val()
   3. 属性操作 attr() removeAttr()
   4. DOM 插入并包裹现有内容 .wrap() .unwrap() .wrapAll() .wrapInner()
   5. DOM 插入现有元素内 .append() .prepend()
   6. DOM 插入现有元素外 .after() .before()
   7. DOM 移除 .empty() .remove()
   8. DOM 替换 .replaceAll() .replaceWith()
3. CSS操作
   1. 尺寸 .css() .height()，.width() .innerHeight()，.innerWidth() .outerHeight()，.outerWidth()
   2. 位置 .offset() .position() .scrollLeft() .scrollTop()
4. 事件处理
   1. 绑定事件处理器 .on() .one() .off()
   2. 鼠标事件 .click() .hover() .mouseenter() .mouseleave() .mousemove() .mouseover() .mouseout()
   3. 表单事件 .focus() .blur() .change() .submit()
   4. 键盘事件 .keydown() .keypress() .keyup()
   5. 浏览器事件 .resize() .scroll()
   6. 事件对象 event.type event.target event.currentTarget event.preventDefault() event.stopPropagation()
5. 遍历
   1. 列表遍历 .map() .each()
   2. 列表中获得一个JS对象的DOM元素 .get()
   3. 树遍历（关系） .children() .find() .next() .parent() .siblings()
6. 动画
   1. .show()
   2. .hide()
   3. .fadeIn()
   4. .fadeOut()

### .show()

执行显示动画

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="./js/jquery-3.6.0.min.js"></script>
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: red;
            display: none;
        }
    </style>
</head>
<body>
    <button>动画</button>
    <div></div>
    <script>
       $("button").click(function(){
           $("div").show(1000)
       })
    </script>
</body>
</html>

```

### .hide()

执行隐藏动画

```html
$("button").click(function(){
    $("div").hide(1000)
})

```

### .fadeIn()

通过淡入的方式显示匹配元素。

```html
$("button").click(function () {
  $("div").fadeIn(1000);
});

```

### .fadeOut()

通过淡出的方式显示匹配元素

```html
$("button").click(function () {
  $("div").fadeOut(1000);
});

```

**实时效果反馈**

**1. 下列是jQuery动画，可以实现淡入效果：**

A show()

B hide()

C fadeIn()

D fadeOut()

**答案**

1=>C

  



 



















