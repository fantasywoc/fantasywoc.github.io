---
layout: post
title:  JavaScript 字符串
date:   2022-05-21 13:10:30 +0300
image:  js封面.png
tags:   study  js

---

# JavaScript 字符串

---

JavaScript 字符串用于存储和处理文本。

字符串可以存储一系列字符，如 "John Doe"。

字符串可以是插入到引号中的任何字符。你可以使用单引号或双引号：var carname = "Volvo XC60";

你可以使用索引位置来访问字符串中的每个字符，字符串的索引从 0 开始，这意味着第一个字符索引值为 [0],第二个为 [1], 以此类推。

```js
var character = carname[7];
```

你也可以在字符串添加转义字符来使用引号：var x = 'It\'s alright';

## String 对象属性

---

| 属性                                                         | 描述                       |
| :----------------------------------------------------------- | :------------------------- |
| [constructor](https://www.runoob.com/jsref/jsref-constructor-string.html) | 对创建该对象的函数的引用   |
| [length](https://www.runoob.com/jsref/jsref-length-string.html) | 字符串的长度               |
| [prototype](https://www.runoob.com/jsref/jsref-prototype-string.html) | 允许您向对象添加属性和方法 |

## String 对象方法

---

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [charAt()](https://www.runoob.com/jsref/jsref-charat.html)   | 返回在指定位置的字符。                                       |
| [charCodeAt()](https://www.runoob.com/jsref/jsref-charcodeat.html) | 返回在指定的位置的字符的 Unicode 编码。                      |
| [concat()](https://www.runoob.com/jsref/jsref-concat-string.html) | 连接两个或更多字符串，并返回新的字符串。                     |
| [endsWith()](https://www.runoob.com/jsref/jsref-endswith.html) | 判断当前字符串是否是以指定的子字符串结尾的（区分大小写）。   |
| [fromCharCode()](https://www.runoob.com/jsref/jsref-fromcharcode.html) | 将 Unicode 编码转为字符。                                    |
| [indexOf()](https://www.runoob.com/jsref/jsref-indexof.html) | 返回某个指定的字符串值在字符串中首次出现的位置。             |
| [includes()](https://www.runoob.com/jsref/jsref-string-includes.html) | 查找字符串中是否包含指定的子字符串。                         |
| [lastIndexOf()](https://www.runoob.com/jsref/jsref-lastindexof.html) | 从后向前搜索字符串，并从起始位置（0）开始计算返回字符串最后出现的位置。 |
| [match()](https://www.runoob.com/jsref/jsref-match.html)     | 查找找到一个或多个正则表达式的匹配。                         |
| [repeat()](https://www.runoob.com/jsref/jsref-repeat.html)   | 复制字符串指定次数，并将它们连接在一起返回。                 |
| [replace()](https://www.runoob.com/jsref/jsref-replace.html) | 在字符串中查找匹配的子串，并替换与正则表达式匹配的子串。     |
| [replaceAll()](https://www.runoob.com/jsref/jsref-replaceall.html) | 在字符串中查找匹配的子串，并替换与正则表达式匹配的所有子串。 |
| [search()](https://www.runoob.com/jsref/jsref-search.html)   | 查找与正则表达式相匹配的值。                                 |
| [slice()](https://www.runoob.com/jsref/jsref-slice-string.html) | 提取字符串的片断，并在新的字符串中返回被提取的部分。         |
| [split()](https://www.runoob.com/jsref/jsref-split.html)     | 把字符串分割为字符串数组。                                   |
| [startsWith()](https://www.runoob.com/jsref/jsref-startswith.html) | 查看字符串是否以指定的子字符串开头。                         |
| [substr()](https://www.runoob.com/jsref/jsref-substr.html)   | 从起始索引号提取字符串中指定数目的字符。                     |
| [substring()](https://www.runoob.com/jsref/jsref-substring.html) | 提取字符串中两个指定的索引号之间的字符。                     |
| [toLowerCase()](https://www.runoob.com/jsref/jsref-tolowercase.html) | 把字符串转换为小写。                                         |
| [toUpperCase()](https://www.runoob.com/jsref/jsref-touppercase.html) | 把字符串转换为大写。                                         |
| [trim()](https://www.runoob.com/jsref/jsref-trim.html)       | 去除字符串两边的空白                                         |
| [toLocaleLowerCase()](https://www.runoob.com/jsref/jsref-tolocalelowercase.html) | 根据本地主机的语言环境把字符串转换为小写。                   |
| [toLocaleUpperCase()](https://www.runoob.com/jsref/jsref-tolocaleuppercase.html) | 根据本地主机的语言环境把字符串转换为大写。                   |
| [valueOf()](https://www.runoob.com/jsref/jsref-valueof-string.html) | 返回某个字符串对象的原始值。                                 |
| [toString()](https://www.runoob.com/jsref/jsref-tostring.html) | 返回一个字符串。                                             |







## JavaScript 运算符

---

| 算术运算符 | 描述         | 赋值运算符 | 例子 | 等同于 |
| :--------- | :----------- | ---------- | ---- | ------ |
| +          | 加法         | =          | x=y  |        |
| -          | 减法         | +=         | x+=y | x=x+y  |
| *          | 乘法         | -=         | x-=y | x=x-y  |
| /          | 除法         | *=         | x*=y | x=x*y  |
| %          | 取模（余数） | /=         | x/=y | x=x/y  |
| ++         | 自增         | %=         | x%=y | x=x%y  |
| x=y++      | 5            |            |      |        |
| --         | 自减         |            |      |        |

## 比较运算符、逻辑运算符

比较运算符在逻辑语句中使用，以测定变量或值是否相等。返回true or false

| 比较运算符 | 描述                                                       | 逻辑运算符 | 描述 | 例子                      |
| :--------- | :--------------------------------------------------------- | ---------- | ---- | ------------------------- |
| ==         | 等于                                                       | &&         | and  | (x < 10 && y > 1) 为 true |
| x==5       | *true*                                                     | \|\|       | or   | (x==5 \|\| y==5) 为 false |
| ===        | 绝对等于（值和类型均相等）                                 | !          | not  | !(x==y) 为 true           |
| x===5      | *true*                                                     |            |      |                           |
| !=         | 不等于                                                     |            |      |                           |
| !==        | 不绝对等于<br>（值和类型有一个不相等，<br>或两个都不相等） |            |      |                           |
| x!==5      | *false*                                                    |            |      |                           |
| >          | 大于                                                       |            |      |                           |
| <          | 小于                                                       |            |      |                           |