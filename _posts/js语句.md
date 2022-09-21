---
layout: post
title:  js 语句
date:   2022-02-05 13:10:30 +0300
image:  js封面.png
tags:   study  js

---

# js语句

## JavaScript 语句标识符

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

## 函数

### 传入参数可以是任意类型，

```js
//函数可以传入任意数据类型的参数
function sayself(o){
console.log(o.address+o.name)
}
var obj={address:"花果山水帘洞",name:"孙悟空"};
sayself(obj);
//return 返回值可以是任意对象，return执行之后便会结束函数
```

```js
(function(){
    console.log("函数定义完立即执行函数，一般只执行一次")
})();
```

### this 关键字

```js
//this用法，一般而言，在Javascript中，this指向函数执行时的当前对象。
//根据调用的不同，this指向不同对象
////以函数形式调用时。this永远都是window。以方法形式调用时，this永远都是调用方法的对象
function myfun(){
    console.log(this.name);
}
var obj1={address:"未知",name:"六耳猕猴",sayname:myfun};
obj.sayname();
obj1.sayname();


```

### 作为函数方法调用函数

在 JavaScript 中, 函数是对象。JavaScript 函数有它的属性和方法。

**call()** 和 **apply()** 是预定义的函数方法。 两个方法可用于调用函数，两个方法的第一个参数必须是对象本身。

```js
function myFunction(a, b) {    return a * b; } 
myObject = myFunction.call(myObject, 10, 2);     // 返回 20
```

```js
function myFunction(a, b) 
{    return a * b; } 
myArray = [10, 2];
myObject = myFunction.apply(myObject, myArray);  // 返回 20
```

两个方法都使用了对象本身作为第一个参数。 两者的区别在于第二个参数： apply传入的是一个参数数组，也就是将多个参数组合成为一个数组传入，而call则作为call的参数传入（从第二个参数开始）。

在 JavaScript 严格模式(strict mode)下, 在调用函数时第一个参数会成为 **this** 的值， 即使该参数不是一个对象。

在 JavaScript 非严格模式(non-strict mode)下, 如果第一个参数的值是 null 或 undefined, 它将使用全局对象替代。

## if条件语句（与c，python类似）

```js
if (condition)
{
  当条件为 true 时执行的代码
}
```

```js
if (condition)
{
  当条件为 true 时执行的代码
}
else
{
  当条件不为 true 时执行的代码
}
```



```js
if (condition1)

  当条件 1 为 true 时执行的代码*
}
else if (condition2)
{
  当条件 2 为 true 时执行的代码
}
else
{
 当条件 1 和 条件 2 都不为 true 时执行的代码
}
```

## switch 语句

请使用 switch 语句来选择要执行的多个代码块之一。

使用 default 关键词来规定匹配不存在时做的事情（也可以不写）

```js
switch(n)
 {      case 1:        
 			执行代码块 1       
 			break;    
 		case 2:        
 			执行代码块 2        
 			break;    
 		default:        
 			与 case 1 和 case 2 不同时执行的代码 
 }
```

## For 循环（与python类似）

for 循环是您在希望创建循环时常会用到的工具。

下面是 for 循环的语法：

```js
for (*语句 1*; *语句 2*; *语句 3*)
{
  *被执行的代码块*
}
```

for 多次循环

```js
for (var i=0; i<5; i++) 
{      
	x="该数字为 " + i + "<br>";
}
```

for 遍历数组

```js
var cars=[1,2,3,4]
for (var i=0,len=cars.length; i<len; i++) 
{     
    document.write(cars[i] + "<br>"); 
}
```

## For/In 循环

JavaScript for/in 语句循环遍历对象的属性：

```js
var person={fname:"Bill",lname:"Gates",age:56};  
for (x in person)  // x 为属性名
{   var txt= ' ';
    txt= person[x]+txt ; 
    document.write(txt)
}
//输出结果为：Bill Gates 56
```

## while 循环(与c语言类似)

while 循环会在指定条件为真时循环执行代码块。

```js
do
{
  需要执行的代码
}
while (条件)
```

## break 语句

break 语句可用于跳出循环。

break 语句跳出循环后，会继续执行该循环之后的代码

## continue 语句

**continue 语句**中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。

有了标签，可以使用break和continue在多层循环的时候控制外层循环。

例如下面：

```js
outerloop:
for (var i = 0; i < 10; i++)
{
    innerloop:
    for (var j = 0; j < 10; j++)
    {
        if (j > 3)
        {
            break;
        }
        if (i == 2)
        {
            break innerloop;
        }
        if (i == 4)
        {
            break outerloop;
        }
        document.write("i=" + i + " j=" + j + "");
    }
}
```

## JavaScript 标签

正如您在 switch 语句那一章中看到的，可以对 JavaScript 语句进行标记。

如需标记 JavaScript 语句，请在语句之前加上冒号：

label: statements

break 和 continue 语句仅仅是能够跳出代码块的语句。

语法:

break labelname;   continue labelname;

continue 语句（带有或不带标签引用）只能用在循环中。

break 语句（不带标签引用），只能用在循环或 switch 中。

通过标签引用，break 语句可用于跳出任何 JavaScript 代码块

## 对象定义

你可以使用字符来定义和创建 JavaScript 对象:

```js
 var person = {
 firstName:"John",
  lastName:"Doe",
  age:50,
  eyeColor:"blue"
};
```

## 访问对象属性

你可以通过两种方式访问对象属性:

```js
person.lastName;
```

## 常见的HTML事件

下面是一些常见的HTML事件的列表:

| 事件        | 描述                         |
| :---------- | :--------------------------- |
| onchange    | HTML 元素改变                |
| onclick     | 用户点击 HTML 元素           |
| onmouseover | 用户在一个HTML元素上移动鼠标 |
| onmouseout  | 用户从一个HTML元素上移开鼠标 |
| onkeydown   | 用户按下键盘按键             |
| onload      | 浏览器已完成页面的加载       |

## JavaScript 可以做什么?

事件可以用于处理表单验证，用户输入，用户行为及浏览器动作:

- 页面加载时触发事件
- 页面关闭时触发事件
- 用户点击按钮执行动作
- 验证用户输入内容的合法性
- 等等 ...

可以使用多种方法来执行 JavaScript 事件代码：

- HTML 事件属性可以直接执行 JavaScript 代码
- HTML 事件属性可以调用 JavaScript 函数
- 你可以为 HTML 元素指定自己的事件处理程序
- 你可以阻止事件的发生。
- 等等 ...

## typeof 操作符

你可以使用 typeof 操作符来检测变量的数据类型。

```js
typeof "John"      // 返回 string
typeof 3.14       // 返回 number
typeof false      // 返回 boolean
typeof [1,2,3,4] // 返回 object//在JavaScript中，数组是一种特殊的对象类型
typeof {name:'John', age:34}// 返回 object
```

