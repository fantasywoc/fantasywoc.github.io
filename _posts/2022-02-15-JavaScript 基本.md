---

layout: post
title:  JavaScript 基本知识
date:   2022-02-15 13:10:30 +0300
image:  js封面.png
tags:   study  js

---



# JavaScript 基本知识

------

JavaScript 没有任何打印或者输出的函数。

## JavaScript 显示数据

JavaScript 可以通过不同的方式来输出数据：

- 使用 **window.alert()** 弹出警告框。
- 使用 **document.write()** 方法将内容写到 HTML 文档中。
- 使用 **innerHTML** 写入到 HTML 元素。
- 使用 **console.log()** 写入到浏览器的控制台。

# 操作 HTML 元素

---

如需从 JavaScript 访问某个 HTML 元素，您可以使用 **document.getElementById(*id*)** 方法。

使用 "id" 属性来标识 HTML 元素， innerHTML 用来获取或插入元素内容：

## 实例

```html
<!DOCTYPE html>
<html>
<body>

<h1>我的第一个 Web 页面</h1>

<p id="demo">我的第一个段落</p>

<script>
document.getElementById("demo").innerHTML = "段落已修改。";
</script>

</body>
</html>
```

以上 JavaScript 语句（在 <script> 标签中）可以在 web 浏览器中执行：

**document.getElementById("demo")** 是使用 id 属性来查找 HTML 元素的 JavaScript 代码 。

**innerHTML = "段落已修改。"** 是用于修改元素的 HTML 内容(innerHTML)的 JavaScript 代码。

![Note](https://m.runoob.com/images/lamp.jpg)**请使用 document.write() 仅仅向文档输出写内容。**

**如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖。**



# JavaScript 语句标识符

---

JavaScript 语句通常以一个 **语句标识符** 为开始，并执行该语句。

语句标识符是保留关键字不能作为变量名使用。

下表列出了 JavaScript 语句标识符 (关键字) ：

| 语句         | 描述                                                         |
| :----------- | :----------------------------------------------------------- |
| break        | 用于跳出循环。                                               |
| catch        | 语句块，在 try 语句块执行出错时执行 catch 语句块。           |
| continue     | 跳过循环中的一个迭代。                                       |
| do ... while | 执行一个语句块，在条件语句为 true 时继续执行该语句块。       |
| for          | 在条件语句为 true 时，可以将代码块执行指定的次数。           |
| for ... in   | 用于遍历数组或者对象的属性（对数组或者对象的属性进行循环操作）。 |
| function     | 定义一个函数                                                 |
| if ... else  | 用于基于不同的条件来执行不同的动作。                         |
| return       | 退出函数                                                     |
| switch       | 用于基于不同的条件来执行不同的动作。                         |
| throw        | 抛出（生成）错误 。                                          |
| try          | 实现错误处理，与 catch 一同使用。                            |
| var          | 声明一个变量。                                               |
| while        | 当条件语句为 true 时，执行语句块。                           |

## 空格

JavaScript 会忽略多余的空格。您可以向脚本添加空格，来提高其可读性。下面的两行代码是等效的：

```js
var person="robob";
var person = "robot";
```

# JavaScript注释

多行注释以 /* 开始，以 */ 结尾。

单行注释以 // 开头

# JavaScript 数据类型

## 变量

可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

- 变量必须以字母开头
- 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
- 变量名称对大小写敏感（y 和 Y 是不同的变量）


JavaScript 变量还能保存其他数据类型，比如文本值 (name="Bill Gates")。

在 JavaScript 中，类似 "Bill Gates" 这样一条文本被称为字符串。

当您向变量分配文本值时，应该用双引号或单引号包围这个值。

当您向变量赋的值是数值时，不要使用引号。一条语句，多个变量

## 变量声明

## **JavaScript 声明提升**

JavaScript 中，函数及变量的声明都将被提升到函数的最顶部。

JavaScript 中，变量可以在使用后声明，也就是变量可以先使用再声明

您可以在一条语句中声明很多变量。该语句以 var 开头，并使用逗号分隔变量即可：

```js
var lastname="Doe", age=30, job="carpenter";
//声明也可横跨多行：
```

```js
var lastname="Doe",
age=30,
job="carpenter";
```

一条语句中声明的多个变量不可以同时赋同一个值:

```html
var x,y,z=1;
```

## 重新声明 JavaScript 变量

如果重新声明 JavaScript 变量，该变量的值不会丢失：

在以下两条语句执行后，变量 carname 的值依然是 "Volvo"：

```js
var carname="Volvo";
var carname;
```

# JavaScript 算数

您可以通过 JavaScript 变量来做算数，使用的是 = 和 + 这类运算符：

```js
y=5; x=y+2;
```

# JavaScript 字面量

在编程语言中，一般固定值称为字面量，如 3.14。

- **数字（Number）字面量** 可以是整数或者是小数，或者是科学计数(e)。3.14 ,1001,123e5
- **字符串（String）字面量** 可以使用单引号或双引号。"John Doe",'John Doe'
- **表达式字面量** 用于计算：5 * 10
- **数组（Array）字面量** 定义一个数组：[40, 100, 1, 5, 25, 10]
- **对象（Object）字面量** 定义一个对象：{firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}
- **函数（Function）字面量** 定义一个函数：function myFunction(a, b) { return a * b;}

JavaScript语言有多种类型的运算符：

| 类型                   | 实例      | 描述                   |
| :--------------------- | :-------- | :--------------------- |
| 赋值，算术和位运算符   | = + - * / | 在 JS 运算符中描述     |
| 条件，比较及逻辑运算符 | == != < > | 在 JS 比较运算符中描述 |

# JavaScript 关键字

JavaScript 关键字用于标识要执行的操作。和其他任何编程语言一样，JavaScript 保留了一些关键字为自己所用。

以下是 JavaScript 中最重要的保留字（按字母顺序）：

| abstract | else       | instanceof | super        |
| -------- | ---------- | ---------- | ------------ |
| boolean  | enum       | int        | switch       |
| break    | export     | interface  | synchronized |
| byte     | extends    | let        | this         |
| case     | false      | long       | throw        |
| catch    | final      | native     | throws       |
| char     | finally    | new        | transient    |
| class    | float      | null       | true         |
| const    | for        | package    | try          |
| continue | function   | private    | typeof       |
| debugger | goto       | protected  | var          |
| default  | if         | public     | void         |
| delete   | implements | return     | volatile     |
| do       | import     | short      | while        |
| double   | in         | static     | with         |

# JavaScript 函数

JavaScript 语句可以写在函数内，函数可以重复引用：

**引用一个函数** = 调用函数(执行函数内的语句)。

```js
function myFunction(a, b) {
  return a * b;     // 返回a乘以b的结果
}
```

# JavaScript 字母大小写

JavaScript 对大小写是敏感的。



