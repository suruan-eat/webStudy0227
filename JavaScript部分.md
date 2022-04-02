# JavaScript基础

## 一、初识

JavaScript是世界上最流行的语言之一，是一种运行在客户端的脚本语言（ Script是脚本的意思

脚本语言∶不需要编译，运行过程中由js解释器(js 引擎)逐行来进行解释并执行

现在也可以基于Node.js技术进行服务器端编程

常用于：

- 表单动态校验（密码强度检测)(JS产生最初的目的)
- 网页特效
  服务端开发(Node.js)
- 桌面程序(Electron)
- App(Cordova)
  控制硬件-物联网(Ruff)
- 游戏开发(cocos2d-js)

浏览器分成两部分︰渲染引擎和JS引擎
·**渲染引擎**：用来解析HTML与CSS，俗称内核，比如chrome浏览器的blink，老版本的webkit。
·**JS引擎**：也称为JS解释器。用来读取网页中的JavaScript代码，对其处理后运行，比如chrome浏览器的V8。
浏览器本身并不会执行JS代码，而是通过内置JavaScript引擎(解释器)来执行S代码。JS引擎执行代码时逐行解释每一句源码（转换为机器语言），然后由计算机去执行，所以JavaScript语言归为脚本语言，会逐行解释执行。

### 1. js组成

![image-20220307215121312](D:\学习web\笔记和图片\web学习笔记\img\image-20220307215121312.png)

#### 1.1 ECMAScript

![image-20220307215328527](D:\学习web\笔记和图片\web学习笔记\img\image-20220307215328527.png)

#### 1.2 DOM--文档对象模型

![image-20220307215500735](D:\学习web\笔记和图片\web学习笔记\img\image-20220307215500735.png)

#### 1.3 BOM--浏览器对象模型

![image-20220307215448534](D:\学习web\笔记和图片\web学习笔记\img\image-20220307215448534.png)

### 2.JS初体验

#### 1.行内式JS

```html
<input type="button" value="lal" onclick="alert('姐姐')">
```

#### 2.内嵌JS

```html
<script>
        alert('luoto');
</script>
```

#### 3，外部JS

```html
 <script src="my.js"></script>
```

注意：此时script内部不能写代码

### 3.JS注释

单行注释：ctrl+/

多行（修改后）：ctrl+shift+/

### 4.JS输入输出语句

![image-20220307221227440](D:\学习web\笔记和图片\web学习笔记\img\image-20220307221227440.png)

```
<script>
        // 输入框
        prompt('请输入年龄');
        // 警示窗
        alert('计算结果是');
        console.log('程序员看到');
</script>
```



## 二、变量

白话:变量就是一个装东西的盒子。
通俗∶变量是用于存放数据的容器。我们通过恋量名获取数据，甚至数据可以修改。

本质:变量是程序在内存中申请的一块用来存放数据的空间。

#### 1.变量的使用

1.声明变量 2.赋值

声明变量：

```
var age;
```

![image-20220308215314978](D:\学习web\笔记和图片\web学习笔记\img\image-20220308215314978.png)

变量赋值：

```
age = 18;
```

3.变量的初始化

```
var mname = 'suruan';
```

#### 2.变量的语法扩展

##### 1.更新变量

变量被重新赋值时，之前的变量值便会被覆盖。

##### 2.声明多个变量

和c语言类似

```
var age = 18,
            address = 'hn',
            gz = '3500';
```

##### 3.声明变量的特殊情况

![image-20220308220705117](D:\学习web\笔记和图片\web学习笔记\img\image-20220308220705117.png)

不声明直接赋值也可以显示（不推荐）

##### 3.变量命名规范

![image-20220308221103012](D:\学习web\笔记和图片\web学习笔记\img\image-20220308221103012.png)

注意：

不要直接用name来定义变量名。

变量名可以$、_ 开头，但不可以&开头。

## 三、数据类型

js 的变量数据类型是只有程序在运行过程中，根据等号右边的值来确定的

JavaScript是一种弱类型或者说动态语言。这意味着不用提前声明变量的类型，在程序运行过程中，类型会被自动确定。

#### 1.简单数据类型（基本数据类型）

![image-20220312211214610](D:\学习web\笔记和图片\web学习笔记\img\image-20220312211214610.png)

##### 1.1 数字型Number

###### 1.数字型进制

常见的进制：二进制、八进制、十进制、十六进制。

八进制：0~7我们程序里面数字前面加0表示八进制

```
var num1 = 010;
console.log(num1);
```

![image-20220312211601420](D:\学习web\笔记和图片\web学习笔记\img\image-20220312211601420.png)

十六进制：0~9 a~f  数字前面加0x

```
var num2 = 0x9, num3 = 0xa;
```

![image-20220312212146428](D:\学习web\笔记和图片\web学习笔记\img\image-20220312212146428.png)

###### 2.数字型范围

最大最小值：

![image-20220312212208721](D:\学习web\笔记和图片\web学习笔记\img\image-20220312212208721.png)

###### 3.数字型三个特殊值

![image-20220312212337766](D:\学习web\笔记和图片\web学习笔记\img\image-20220312212337766.png)

isNaN( )这个方法用来判断非数字―并且返回一个值如果是数字返回的是 false 如果不是数字返回的是true.

##### 1.2 字符串行String

![image-20220312212759338](D:\学习web\笔记和图片\web学习笔记\img\image-20220312212759338.png)

![image-20220312212830168](D:\学习web\笔记和图片\web学习笔记\img\image-20220312212830168.png)

###### 1.字符转义符

![image-20220312213031483](D:\学习web\笔记和图片\web学习笔记\img\image-20220312213031483.png)

```
var str = 'hahahahah\nhhhh'
console.log(str);
```

###### 2.字符串长度

通过length来检查字符串长度（包括空格）。

```
var str = 'happy day';
console.log(str.length);
```

###### 3.字符串拼接 " + "

多个字符串之间可以使用“+”进行拼接，其拼接方式为字符串＋任何类型=拼接之后的新字符串。

拼接前会把与字符串相加的任何类型转成字符串，再拼接成一个新的字符串。

只要有字符串和其他类型相拼接最终的结果是字符串类型。

![image-20220312214336765](D:\学习web\笔记和图片\web学习笔记\img\image-20220312214336765.png)

```
console.log('12' + '12');
console.log(12 + 12);
```

![image-20220312214432251](D:\学习web\笔记和图片\web学习笔记\img\image-20220312214432251.png)

注意区分NaN:

```
console.log('hhhh' + 100);
console.log('hhhh' - 100);
```

![image-20220312214751434](D:\学习web\笔记和图片\web学习笔记\img\image-20220312214751434.png)

##### 1.3布尔型Boolean

![image-20220312215524157](D:\学习web\笔记和图片\web学习笔记\img\image-20220312215524157.png)

##### 1.4 Undefined 和 Null

undefined是指变量未被赋值

![image-20220312215657578](D:\学习web\笔记和图片\web学习笔记\img\image-20220312215657578.png)

null是指给变量赋值为null，即表明变量存值为空

![image-20220312215750907](D:\学习web\笔记和图片\web学习笔记\img\image-20220312215750907.png)

#### 2.获取变量数据类型 

##### 2.1 typeof

```
		var num = 10;
        console.log(typeof num);
        var str = 'suruan';
        console.log(typeof str);
        var flag = true;
        console.log(typeof flag);
```

注意：

null属于对象（object）

prompt取过来的值为字符型

也可以通过控制台颜色来判断:

```
		console.log('18');
        console.log(18);
        console.log(true);
        console.log(null);
```

![image-20220312221002968](D:\学习web\笔记和图片\web学习笔记\img\image-20220312221002968.png)

##### 2.2 字面量

![image-20220312220825976](D:\学习web\笔记和图片\web学习笔记\img\image-20220312220825976.png)

#### 3.数据类型转换

##### 1.转换为字符串型

![image-20220312221133156](D:\学习web\笔记和图片\web学习笔记\img\image-20220312221133156.png)

1. 变量.toString

```
var num = 10;
var str = num.toString();
```

2. String(变量)

```
var num2 = 10;
console.log(String(num2));
```

2. 字符串拼接（隐式转换）

```
		var num3 = 8;
        console.log(num3);
        console.log(num3 + ' ');
```

##### 2.转换为数字型

![image-20220312222253029](D:\学习web\笔记和图片\web学习笔记\img\image-20220312222253029.png)

###### 1.parseInt( )

```
var age = prompt('input age');
console.log(parseInt(age));
```

注意：

转换后会变成整数

如果跟了单位则会去掉单位

如果数字前有字符则无法识别，出现NaN

```
console.log(parseInt('3.14'));
        console.log(parseInt('3.14px'));
        console.log(parseInt('PI3.14px'));
```

![image-20220312222749329](D:\学习web\笔记和图片\web学习笔记\img\image-20220312222749329.png)

###### 2.parseFloat( )

```
console.log(parseFloat('3.14px'));
        console.log(parseFloat('PI3.14px'));
```

![image-20220312223125702](D:\学习web\笔记和图片\web学习笔记\img\image-20220312223125702.png)

###### 3.Number( )

```
var str = '123';
        console.log(Number(str));
```

###### 4.隐式转换

```
		console.log('12' - 0);
        console.log('123' - '120');
        console.log('123' * 1);
```

##### 3.转换为布尔型

![image-20220312224637211](D:\学习web\笔记和图片\web学习笔记\img\image-20220312224637211.png)

![image-20220312224654053](D:\学习web\笔记和图片\web学习笔记\img\image-20220312224654053.png)

### 解释型语言和编译行语言

![image-20220312224923475](D:\学习web\笔记和图片\web学习笔记\img\image-20220312224923475.png)

![image-20220312224944681](D:\学习web\笔记和图片\web学习笔记\img\image-20220312224944681.png)

### 标识符、关键字、保留字

#### 标识符

就是指开发人员为变量、属性、函数、参数取的名字

标识符不能是关键字或保留字。

#### 关键字

是指JS本身已经使用了的字，不能再用它们充当变量名、方法名。

![image-20220312225200943](D:\学习web\笔记和图片\web学习笔记\img\image-20220312225200943.png)

#### 保留字

实际上就是预留的“关键字”，意思是现在虽然还不是关键字，但是未来可能会成为关键字，同样不能使用它们当变量名或方法名。

![image-20220312225253404](D:\学习web\笔记和图片\web学习笔记\img\image-20220312225253404.png)



## 四、运算符

运算符( operator )：也被称为操作符，是用于实现赋值、比较和执行算数运算等功能的符号。

#### 1.算术运算符

![image-20220313182124425](D:\学习web\笔记和图片\web学习笔记\img\image-20220313182124425.png)

注意：

浮点数运算会有精度问题，不能直接判断两个浮点数相等。

算术运算符有优先级

##### 1.表达式和返回值

**表达式︰**是由数字、运算符、变量等以能求得数值的有意义排列方法所得的组合

简单理解∶是由数字、运算符、变量等组成的式子

表达式最终返回的结果为**返回值**。

#### 2.自加、自减运算符

```
num++;/++num;(前置递增/后置递增)
num--;/--num;
```

二者区别：和c语言差不多。

后置使用时，是返回值，再自增

```
		var num = 1;
        console.log(num++);
        console.log(num);
```

![image-20220313202748787](D:\学习web\笔记和图片\web学习笔记\img\image-20220313202748787.png)

前置使用时，是先自增，再返回值

```
		var num = 1;
        console.log(++num);
```

注意理解（可以将其拆分步骤来理解）：

```
		var e = 10;
        var f = e++ + ++e;
        console.log(f);
        
        var e = 10;
        var g = e++;
        console.log(g);
        g = g + ++e;
        console.log(g);
```

![image-20220313203950831](D:\学习web\笔记和图片\web学习笔记\img\image-20220313203950831.png)

#### 3.比较运算符

![image-20220313204144300](D:\学习web\笔记和图片\web学习笔记\img\image-20220313204144300.png)

注意：

1．我们程序里面的等于符号是==默认转换数据类型会把字符串型的数据转换为数字型

![image-20220313204318687](D:\学习web\笔记和图片\web学习笔记\img\image-20220313204318687.png)

 2．我们程序里面有全等一模一样要求两侧的值还有数据类型完全一致才可以true

![image-20220313204513881](D:\学习web\笔记和图片\web学习笔记\img\image-20220313204513881.png)

![image-20220313204436891](D:\学习web\笔记和图片\web学习笔记\img\image-20220313204436891.png)

#### 4.逻辑运算符

![image-20220313204748662](D:\学习web\笔记和图片\web学习笔记\img\image-20220313204748662.png)

##### 短路运算（逻辑中断）

**短路运算的原理︰**当有多个表达式(值)时,左边的表达式值可以确定结果时,就不再继续运算右边的表达式的值;

###### 1.逻辑与

![image-20220313205416696](D:\学习web\笔记和图片\web学习笔记\img\image-20220313205416696.png)

```
		console.log(123 && 456);
        console.log(0 && 123);
```

![image-20220313205750069](D:\学习web\笔记和图片\web学习笔记\img\image-20220313205750069.png)

![image-20220313205714428](D:\学习web\笔记和图片\web学习笔记\img\image-20220313205714428.png)

###### 2.逻辑或

逻辑或短路运算：

![image-20220313210416616](D:\学习web\笔记和图片\web学习笔记\img\image-20220313210416616.png)

![image-20220313210508981](D:\学习web\笔记和图片\web学习笔记\img\image-20220313210508981.png)

注意：

当第一个式子为真时，便不会执行第二个式子（即产生中断）。

```
		var num = 0;
        console.log(123 || num++);
        console.log(num);
```

![image-20220313210658738](D:\学习web\笔记和图片\web学习笔记\img\image-20220313210658738.png)

#### 5.赋值运算符

![image-20220313210910270](D:\学习web\笔记和图片\web学习笔记\img\image-20220313210910270.png)

#### 6.运算符优先级

![image-20220313211221772](D:\学习web\笔记和图片\web学习笔记\img\image-20220313211221772.png)

一元运算符中逻辑非!优先级最高

逻辑与比逻辑或优先级高

## 五、JS流程控制

流程控制主要有三种结构，分别是**顺序结构、分支结构和循环结构**，这三种结构代表三种代码执行的顺序。

![image-20220313212052474](D:\学习web\笔记和图片\web学习笔记\img\image-20220313212052474.png)

### 1.分支流程控制

#### 1.1 if else双分支语句

```
var num = 1;
        if (num == 1) {
            num++;
        }
        else {
            num = 10;
        }

        console.log(num);
```

![image-20220313212628077](D:\学习web\笔记和图片\web学习笔记\img\image-20220313212628077.png)

##### if else if多分支语句

```
var age = prompt('请输入你的年龄：');
        if (age >= 18) {
            alert('欢迎光临');
        }
        else if (age <= 10) {
            alert('nono');
        } else {
            alert('抱歉，您的年龄未达要求');
        }
```

#### 2.三元表达式

语法：

```
条件表达式 ？ 表达式1 ： 表达式2
var num = 10;
        var result = num > 20 ? 'true' : 'false';
        console.log(result);
```

如果表达式为真，返回表达式1的值，为假，则返回表达式2的值。

#### 3.多分支语句 switch

switch语句也是多分支语句，它用于基于不同的条件来执行不同的代码。当要针对变量设置一系列的**特定值**的选项时，就可以使用switch。

![image-20220313222946894](D:\学习web\笔记和图片\web学习笔记\img\image-20220313222946894.png)

![image-20220313223424526](D:\学习web\笔记和图片\web学习笔记\img\image-20220313223424526.png)

```
var num = 1;
        switch (num) {
            case 1:
                console.log('1');
                break;
            case 2:
                console.log('2');
                break;
            default:
                console.log('no');

        }
```

注意：

num 的值和case里面的值相匹配的时候是全等，必须是值和数据类型一致才可以num === 1

如果case里没有break，则会将下一个的数据也输出。

#### 4.if else if语句和switch语句区别

![image-20220313224847564](D:\学习web\笔记和图片\web学习笔记\img\image-20220313224847564.png)

### 2.循环

#### 1.for循环

![image-20220314163124034](D:\学习web\笔记和图片\web学习笔记\img\image-20220314163124034.png)

断点调试：

![image-20220314165302536](D:\学习web\笔记和图片\web学习笔记\img\image-20220314165302536.png)

#### 2.while循环

![image-20220314192428326](D:\学习web\笔记和图片\web学习笔记\img\image-20220314192428326.png)

#### 3.do while循环

至少循环一次。

![image-20220314193328790](D:\学习web\笔记和图片\web学习笔记\img\image-20220314193328790.png)

#### 4.continue，break

continue：

会直接退出当前次的循环，不会执行continue下面的循环，继续其他次数的循环。

![image-20220314193713000](D:\学习web\笔记和图片\web学习笔记\img\image-20220314193713000.png)

break：

退出整个循环，不会执行之后次数的循环次。

![image-20220314194049704](D:\学习web\笔记和图片\web学习笔记\img\image-20220314194049704.png)

## 六、数组

![image-20220314195335549](D:\学习web\笔记和图片\web学习笔记\img\image-20220314195335549.png)

#### 1.数组的创建

##### 1.利用new创建数组

```
var arr = new Array();
```

##### 2. 利用数组字面量创建数组

```
var arr = [];
```

![image-20220314200437898](D:\学习web\笔记和图片\web学习笔记\img\image-20220314200437898.png)

#### 2.数组的索引

![image-20220314200800814](D:\学习web\笔记和图片\web学习笔记\img\image-20220314200800814.png)

#### 3.数组的遍历

用for循环

#### 4.数组长度

数组名.length

动态监测数组元素的个数

#### 5.数组中新增元素

1.通过修改length长度（length属性是可读写的）

未给值的会默认为undefined

2.修改索引号，追加数组元素

注意：

不能直接给数组名赋值，否则会覆盖掉以前的数据

###### 一个有意思的小例子：

![image-20220314202854259](D:\学习web\笔记和图片\web学习笔记\img\image-20220314202854259.png)

#### 6.冒泡排序

```html
var arr = [3, 1, 9, 2, 5, 6];
        var temp;
        for (i = 0; i < arr.length - 1; i++) {
            //外层表示趟数
            for (var j = 0; j <= arr.length - i - 1; j++) {
                //里层循环表每趟遍历的次数，每次都会将最大的数归位
                if (arr[j] > arr[j + 1]) {
                    temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
        console.log(arr);
```

## 七、函数

**函数︰**就是封装了一段可被重复调用执行的代码块。通过此代码块可以实现大量代码的重复使用。

### 1.函数的使用

#### 1.声明函数

关键字function

函数名一般用动词

```
function 函数名(){
   函数体;
}
```

#### 2.调用函数

```
函数名();
```

#### 3.函数的封装

函数的封装是把一个或者多个功能通过函数的方式封装起来，对外只提供一个简单的函数接口。

### 2.函数的参数

函数可以带参数也可以不带参数。

#### 1.形参和实参

```
function 函数名(形参1){ //声明函式小括号里是形参，用于接收实参，相当于一个变量
   函数体;
}
函数名(实参1); //调用函式小括号里是实参
```

注意：

多个参数逗号隔开

如果实参个数大于形参个数，会取到形参的个数

如果实参个数小于形参个数，多余的形参会定义为undefined，结果为NaN

### 3.函数的返回值

#### 1. return 返回函数![image-20220314214356174](D:\学习web\笔记和图片\web学习笔记\img\image-20220314214356174.png)

```
function getSum() {
            var sum = 0;
            for (var i = 1; i <= 100; i++) {
                sum += i;
            }
            // console.log(sum);
            return sum;
        }
        console.log(getSum());
```

#### 2.return 终止函数

即return后面的代码不会被执行。

注意：

return只能返回一个值。如果用逗号隔开多个值，以最后一个为准。

若要返回多个值，可以返回一个数组。

如果函数没有return，则返回undefined

### 4.arguments的使用

只有函数才有arguments对象，且每个函数内置好了arguments

![image-20220314223917373](D:\学习web\笔记和图片\web学习笔记\img\image-20220314223917373.png)

当我们不确定有多少个参数传递的时候，可以用arguments来获取。在JavaScript中,arguments实际上它是当前函数的一个内置对象。所有函数都内置了一个arguments对象，arguments对象中存储了传递的所有实参。
arguments展示形式是一个伪数组，因此可以进行遍历。伪数组具有以下特点︰

●具有length属性
●按索引方式储存数据（形如数组）
●不具有数组的push , pop等方法

### 5.函数是可以相互调用的

```
function fn1() {
            console.log(11);
            fn2();
        }
        fn1();
        function fn2() {
            console.log(22);
        }
```

### 6.函数的两种声明方式

#### 1.关键字

#### 2.函数表达式

![image-20220314230501133](D:\学习web\笔记和图片\web学习笔记\img\image-20220314230501133.png)

## 八、JS作用域

### 1.作用域

解决命名冲突问题

![image-20220314230909777](D:\学习web\笔记和图片\web学习笔记\img\image-20220314230909777.png)

### 2.变量的作用域

#### 1.全局变量

![image-20220314231418318](D:\学习web\笔记和图片\web学习笔记\img\image-20220314231418318.png)

这时，函数内部即使没有声明该变量也可以使用。

#### 2.局部变量

![image-20220314231434603](D:\学习web\笔记和图片\web学习笔记\img\image-20220314231434603.png)

#### 3.区别

![image-20220314231453254](D:\学习web\笔记和图片\web学习笔记\img\image-20220314231453254.png)

### 3.块级作用域（es6之后）

![image-20220314231819786](D:\学习web\笔记和图片\web学习笔记\img\image-20220314231819786.png)

### 4.作用域链

![image-20220314232206350](D:\学习web\笔记和图片\web学习笔记\img\image-20220314232206350.png)

作用域链:

内部函数访问外部函数的变量，采取的是链式查找的方式来决定取那个值这种结构我们称为作用域链，就近原则

![image-20220314232138176](D:\学习web\笔记和图片\web学习笔记\img\image-20220314232138176.png)

## 九、JS预解析

1．我们js引擎运行js分为两步:  预解析代码执行

(1)．预解析js引擎会把js里面所有的 var 还有 function 提升到当肌作用域的最肌阻

(2)．代码执行按照代码书写的顺序从上往下执行

2．预解析分为变量预解析（变量提升）和函数预解析（函数提升）
(1)变量提升就是把所有的变量声明提升到当前的作用域最前面,但是不提升赋值操作

![image-20220314233143613](D:\学习web\笔记和图片\web学习笔记\img\image-20220314233143613.png)

![image-20220314233406995](D:\学习web\笔记和图片\web学习笔记\img\image-20220314233406995.png)

因此，函数表达式的调用要写在函数表达式的下面。

(2）函数提升就是把所有的函数声明提升到当前作用域的最前面，不调用函数

![image-20220314233546993](D:\学习web\笔记和图片\web学习笔记\img\image-20220314233546993.png)

##### 小例子：

```
var num = 10;
        fun();
        function fun() {
            console.log(num);
            var num = 20;
        }

        //相当于执行
        var num;
        function fun() {
            var num;
            console.log(num);  //undefined
            num = 20;
        }
        num = 10;
        fun();

```

```
var num = 10;
        function fn() {
            console.log(num);
            var num = 20;
            console.log(num);
        }
        fn();
        //相当于执行
        var num;
        function fn() {
            var num;
            console.log(num); //undefined
            num = 20;
            console.log(num); //20
        }
        num = 10;
        fn();

```

```
var a = 18;
        f1();
        function f1() {
            var b = 9;
            console.log(a);
            console.log(b);
            var a = '123';
        }
        //相当于执行
        var a;
        function f1() {
            var b;
            var a
            b = 9;
            console.log(a);//undefined
            console.log(b);//9
            a = '123';
        }
        a = 18;
        f1();
```

```
f1();
        console.log(c);
        console.log(b);
        console.log(a);
        function f1() {
            var a = b = c = 9;
            //相当于var a = 9; b = 9; c = 9; 此时b，c为全局变量
            //而集体声明是： var a = 9, b = 9, c = 9;
            console.log(a);
            console.log(b);
            console.log(c);
        }
        //相当于执行
        function f1() {
            var a;
            a = b = c = 9;
            console.log(a);
            console.log(b);
            console.log(c);
        }
        f1();
        console.log(c);
        console.log(b);
        console.log(a);
```

## 十、JS对象

在JavaScript中，对象是一组无序的相关**属性**和**方法**的集合，所有的事物都是对象，例如字符串、数值、数组、函数等。

对象是由属性和方法组成的。

属性︰事物的特征，在对象中用属性来表示(常用名词)

方法:事物的行为，在对象中用方法来表示(常用动词)

![image-20220315152348651](D:\学习web\笔记和图片\web学习笔记\img\image-20220315152348651.png)

### 1.创建对象的三种方式（自定义对象）

#### 1.1 利用字面量创建对象

属性或者方法采用键值对的形式

![image-20220315153017145](D:\学习web\笔记和图片\web学习笔记\img\image-20220315153017145.png)

##### 1.使用对象：

1.调用对象的属性的两种方式：

（1）对象名.属性名

```
alert(obj.age);
```

（2）对象名['属性名']

```
alert(obj['sex']);
```

2.调用对象的方法：

对象名.方法名();

```
obj.haveFun();
```



##### 2.变量、属性、函数、方法的区别

1.变量和属性

相同点：

​	都是用来存储数据

区别：

​	变量单独声明并赋值使用的时候直接写变量名单独存在

​	属性在对象里面的不需要声明的使用的时候必须是对象.属性

 2．函数和方法

相同点：

​	都是实现某种功能做某件事

区别：

​	函数是单独声明并且调用的函数名()单独存在的

​	方法在对象里面调用的时候对象.方法()

##### 1.遍历对象 for...in

语法：

for (变量 in 对象)

变量通常写为k或者key

![image-20220316211010661](D:\学习web\笔记和图片\web学习笔记\img\image-20220316211010661.png)

```
for (var k in obj) {
            console.log(k);
            console.log(obj[k]);
        }
```



#### 1.2 利用new Object创建对象

![image-20220315155425274](D:\学习web\笔记和图片\web学习笔记\img\image-20220315155425274.png)



#### 1.3利用构造函数创建对象

因为我们一次创建一个对象，里面很多的属性和方法是大量相同的我们只能复制

因此我们可以利用函数的方法重复这些相同的代码我们就把这个函数称为构造函数

又因为这个函数不一样，里面封装的不是普通代码，而是对象

构造函数就是把我们对象里面一些相同的属性和方法抽象出来封装到函数里面

![image-20220316151708963](D:\学习web\笔记和图片\web学习笔记\img\image-20220316151708963.png)

![image-20220316151824443](D:\学习web\笔记和图片\web学习笔记\img\image-20220316151824443.png)

![image-20220316160839668](D:\学习web\笔记和图片\web学习笔记\img\image-20220316160839668.png)

```
function School(uname, age, sex) {
            this.name = uname;
            this.age = age;
            this.sex = sex;
            this.eat = function (food) {
                alert(food);
            }
        }
        var susu = new School('suruan', 22, 'female');
        console.log(typeof susu);
        console.log(susu.name);
        susu.eat('酥肉');
```

##### 1.**构造函数和对象**

构造函数，如Stars()，抽象了对象的公共部分，封装到了函数里面，它泛指某一大类( class )
创建对象，如new Stars()，特指某一个，通过new关键字创建对象的过程我们也称为对象实例化

##### 2.new关键字

![image-20220316163751181](D:\学习web\笔记和图片\web学习笔记\img\image-20220316163751181.png)

![image-20220316163808754](D:\学习web\笔记和图片\web学习笔记\img\image-20220316163808754.png)

### 2. JS内置对象

![image-20220317000346159](D:\学习web\笔记和图片\web学习笔记\img\image-20220317000346159.png)

![image-20220317000424247](D:\学习web\笔记和图片\web学习笔记\img\image-20220317000424247.png)

#### 1.查文档

![image-20220317000825558](D:\学习web\笔记和图片\web学习笔记\img\image-20220317000825558.png)

#### 2.Math()对象

查阅MDN文档：

与其他全局对象不同的是，`Math` 不是一个构造器。`Math` 的所有属性与方法都是静态的。引用圆周率的写法是 `Math.PI`，调用正余弦函数的写法是 `Math.sin(x)`，`x` 是要传入的参数。`Math` 的常量是使用 JavaScript 中的全精度浮点数来定义的。

Math对象不是构造函数，它具有数学常数和函数的属性和方法。跟数学相关的运算（求绝对值，取整、最大值等）可以使用Math中的成员。

![image-20220317002301465](D:\学习web\笔记和图片\web学习笔记\img\image-20220317002301465.png)

注意：

abs会将字符型进行隐式转换为数字型

![image-20220317002643305](D:\学习web\笔记和图片\web学习笔记\img\image-20220317002643305.png)

##### 2.1 Math对象随机数

`**Math.random()**` 函数返回一个浮点数,  伪随机数在范围从**0到**小于**1**（0<= x <1）

这个方法里不跟参数

得到一个两数之间的随机整数：

```
function getRandomArbitrary(min, max) {
  return Math.floor(Math.random() * (max - min) + min);
}
```

#### 3.日期对象Date()

日期对象是一个构造函数，必须用new来调用日期对象

如果括号里没有参数，如果没有提供参数，那么新创建的Date对象表示实例化时刻的日期和时间。

有参数：

![image-20220317204938407](D:\学习web\笔记和图片\web学习笔记\img\image-20220317204938407.png)

```
var date = new Date();
        console.log(date);
        var date1 = new Date(2012, 10, 1); //注意：数字型的显示出来会比实际大一个月
        console.log(date1);
        var date2 = new Date('2012-10-1');
        console.log(date2);
```

![image-20220317205943556](D:\学习web\笔记和图片\web学习笔记\img\image-20220317205943556.png)

##### 1.日期格式化

![image-20220317210058310](D:\学习web\笔记和图片\web学习笔记\img\image-20220317210058310.png)

```
//格式化日期
        var date = new Date();
        var year = date.getFullYear();
        var month = date.getMonth() + 1;
        var dates = date.getDate();
        var week = date.getDay();
        var arr = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
        console.log('今天是：' + year + '年' + month + '月' + dates + '日' + arr[week]);
```

```
//格式化时分秒
        function getTime() {
            var time = new Date();
            var h = time.getHours();
            h = h < 10 ? '0' + h : h;
            var m = time.getMinutes();
            m = m < 10 ? '0' + m : m;
            var s = time.getSeconds();
            s = s < 10 ? '0' + s : s;
            return h + ':' + m + ':' + s;
        }
        console.log(getTime());
```

##### 2.通过Date获得现在距离过去的毫秒数（时间戳）

![image-20220317212537600](D:\学习web\笔记和图片\web学习笔记\img\image-20220317212537600.png)

##### 3.倒计时案例

![image-20220317214711864](D:\学习web\笔记和图片\web学习笔记\img\image-20220317214711864.png)

```
function countDown(time) {
            var nowTime = +new Date();//当前时间的时间戳
            var inputTime = +new Date(time); //用户输入时间的时间戳
            var times = (inputTime - nowTime) / 1000; //剩余时间戳的秒数
            var d = parseInt(times / 60 / 60 / 24);
            d = d < 10 ? '0' + d : d;
            var h = parseInt(times / 60 / 60 % 24);
            h = h < 10 ? '0' + h : h;
            var m = parseInt(times / 60 % 60);
            m = m < 10 ? '0' + m : m;
            var s = parseInt(times % 60);
            s = s < 10 ? '0' + s : s;
            return d + '天' + h + '时' + m + '分' + s + '秒';

        }
        console.log(countDown('2022-3-17 22:0:0'));
        var date = Date();
        console.log(date);
```

#### 4.数组对象

1.利用数组字面量

```
var arr = [1,2,3];
```

2.利用new Array()

![image-20220317225948185](D:\学习web\笔记和图片\web学习笔记\img\image-20220317225948185.png)

##### 1.检测是否为数组

（1）instanceof

![image-20220317230154329](D:\学习web\笔记和图片\web学习笔记\img\image-20220317230154329.png)

（2）Array.isArray(参数) H5新增

![image-20220317230444174](D:\学习web\笔记和图片\web学习笔记\img\image-20220317230444174.png)

##### 2.添加删除数组元素

![image-20220317230555255](D:\学习web\笔记和图片\web学习笔记\img\image-20220317230555255.png)

###### 1.push

后面添加

```
var arr = [1, 2];
        console.log(arr.push(3));;
        console.log(arr);
```

![image-20220317230757943](D:\学习web\笔记和图片\web学习笔记\img\image-20220317230757943.png)

###### 2.unshift

前面添加

![image-20220317230954103](D:\学习web\笔记和图片\web学习笔记\img\image-20220317230954103.png)

###### 3.pop

删除数组最后的一个元素

![image-20220317231121054](D:\学习web\笔记和图片\web学习笔记\img\image-20220317231121054.png)

###### 4.shift

删除数组第一个元素

![image-20220317231148331](D:\学习web\笔记和图片\web学习笔记\img\image-20220317231148331.png)

##### 3.数组翻转、数组排序

![image-20220317231635417](D:\学习web\笔记和图片\web学习笔记\img\image-20220317231635417.png)

注意：数组排序sort会有一定错误

```
var arr1 = [13, 1, 12, 2, 33];
        arr1.sort();
        console.log(arr1);
```

![image-20220317232037763](D:\学习web\笔记和图片\web学习笔记\img\image-20220317232037763.png)

简单使用 sort 方法的时候，是按位排序的

正确写法：

```
var arr1 = [13, 1, 12, 2, 33];
        arr1.sort(function (a, b) {
            return a - b; //升序排列
            // return b - a;//降序排列
        });
        console.log(arr1);
```

如果a-b>0(即正数)就把a和b的位置交换，也就是较小的一个数会排到前面；
如果b-a>0就把a和b的位置交换，也就是较大的一个数会排到前面。

原理可以参考：[(4条消息) sort(function(a,b){return a -b})函数排序问题_先飞小笨鸟的博客-CSDN博客](https://blog.csdn.net/qq_43058026/article/details/104531495)

##### 4.数组索引方法

![image-20220317233802110](D:\学习web\笔记和图片\web学习笔记\img\image-20220317233802110.png)

indexOf()从前往后查找

![image-20220317233948288](D:\学习web\笔记和图片\web学习笔记\img\image-20220317233948288.png)

lastindexOf()从后往前查找

![image-20220317234051172](D:\学习web\笔记和图片\web学习笔记\img\image-20220317234051172.png)

###### 数组去重例子（面试）

![image-20220317235019987](D:\学习web\笔记和图片\web学习笔记\img\image-20220317235019987.png)

```
function unique(arr) {
            var newArr = [];
            for (var i = 0; i < arr.length; i++) {
                if (newArr.indexOf(arr[i]) === -1) //在新数组中检查是否有重复,-1即没有重复，放入即可
                {
                    newArr.push(arr[i]);
                }
            }
            return newArr;
        }
        var demo = unique(['a', 'c', 'd', 'e', 'a', 'c']);
        console.log(demo);
```

##### 5.字符转换为字符串

![image-20220317235321822](D:\学习web\笔记和图片\web学习笔记\img\image-20220317235321822.png)

```
var arr = [1, 2, 3];
        console.log(arr.toString(arr));
        var arr1 = [1, 2, 3];
        console.log(arr.join('-'));
```

join可以选择分隔符。

##### 6.其他方法

![image-20220317235601458](D:\学习web\笔记和图片\web学习笔记\img\image-20220317235601458.png)

#### 5.字符串对象

##### 1.基本包装类型：

![image-20220319210629051](D:\学习web\笔记和图片\web学习笔记\img\image-20220319210629051.png)

![image-20220319210702930](D:\学习web\笔记和图片\web学习笔记\img\image-20220319210702930.png)

##### 2.字符串的不可变性

字符串里的值不可变，虽然看上去可以改变内容，但是地址变了，内存中开辟了一个新的内存空间

![image-20220319211103054](D:\学习web\笔记和图片\web学习笔记\img\image-20220319211103054.png)

##### 3.根据字符返回位置

字符串所有的方法，都不会修改字符串本身(字符串是不可变的)，操作完成会返回一个新的字符串。

![image-20220319211337550](D:\学习web\笔记和图片\web学习笔记\img\image-20220319211337550.png)

```
var str = '改革春风吹满地，春天来了';
        console.log(str.indexOf('春'));
        console.log(str.indexOf('春', 3));//从str[3]开始查找
```

##### 4.根据位置返回字符

![image-20220319213004343](D:\学习web\笔记和图片\web学习笔记\img\image-20220319213004343.png)

![image-20220319213319810](D:\学习web\笔记和图片\web学习笔记\img\image-20220319213319810.png)

```
//遍历字符串
        var str = 'suruan';
        for (var i = 0; i < str.length; i++) {
            console.log(str.charAt(i));
        }
```

##### 5.字符串操作方法

![image-20220319221152383](D:\学习web\笔记和图片\web学习笔记\img\image-20220319221152383.png)

![image-20220319221503333](D:\学习web\笔记和图片\web学习笔记\img\image-20220319221503333.png)

![image-20220319221755262](D:\学习web\笔记和图片\web学习笔记\img\image-20220319221755262.png)

![image-20220319222433548](D:\学习web\笔记和图片\web学习笔记\img\image-20220319222433548.png)

![image-20220319222454831](D:\学习web\笔记和图片\web学习笔记\img\image-20220319222454831.png)

## 十一、JS简单数据类型和复杂数据类型

简单类型又叫做基本数据类型或者值类型，复杂类型又叫做引用类型。
**值类型:**简单数据类型/基本数据类型，在存储时变量中存储的是值本身，因此叫做值类型string , number, boolean , undefined , null
**引用类型∶**复杂数据类型，在存储时变量中存储的仅仅是地址(引用），因此叫做引用数据类型通过new关键字创建的对象（系统对象、自定义对象），如Object、Array、Date等

![image-20220319230821734](D:\学习web\笔记和图片\web学习笔记\img\image-20220319230821734.png)

### 1.栈和堆

![image-20220319231030312](D:\学习web\笔记和图片\web学习笔记\img\image-20220319231030312.png)

### 2.简单类型的内存分配

![image-20220319231705002](D:\学习web\笔记和图片\web学习笔记\img\image-20220319231705002.png)

### 3.复杂类型的数据分配

![image-20220319231834972](D:\学习web\笔记和图片\web学习笔记\img\image-20220319231834972.png)

1．简单数据类型是存放在栈里面里面直接开辟一个空间，存放的是值
2．复杂数据类型首先在栈里面存放地址十六进制表示―然后这个地址指向堆里面的数据

### 4.简单类型传参

函数的形参也可以看做是一个变量，当我们把一个值类型变量作为参数传给函数的形参时，其实是把变量在栈空间里的值复制了一份给形参，那么在方法内部对形参做任何修改，都不会影响到的外部变量

### 5.复杂类型传参

函数的形参也可以看做是一个变量，当我们把引用类型变量传给形参时，其实是把变量在栈空间里保存的堆地址复制给了形参，形参和实参其实保存的是同一个堆地址，所以操作的是同一个对象。

参考理解：

![image-20220319232534441](D:\学习web\笔记和图片\web学习笔记\img\image-20220319232534441.png)

# Web APIs部分

**API：**

APl ( Application Programming Interface,应用程序编程接口)是一些预先定义的函数，目的是提供应用程序与开发人员基于某软件或硬件得以访问一组例程的能力，而又无需访问源码，或理解内部工作机制的细节。
简单理解︰API是给程序员提供的一种工具，以便能更轻松的实现想要完成的功能。

**Web API：**

Web API是浏览器提供的一套操作浏览器功能和页面元素的API( BOM和DOM)。
现阶段我们主要针对于浏览器讲解常用的API，主要针对浏览器做交互效果。比如我们想要浏览器弹出一个警示框，直接使用alert(‘弹出’)
MDN详细APl : https://developer.mozilla.org/zh-CN/docs/Web/API

因为WebAPI很多，所以我们将这个阶段称为Web APIs

**区别：**

1.API是为我们程序员提供的一个接口，帮助我们实现某种功能，我们会使用就可以了，不必纠结内部如何实现2.Web API主要是针对于浏览器提供的接口，主要针对于浏览器做交互效果。
3.Web API一般都有输入和输出（函数的传参和返回值），WebAPI很多都是方法（函数)

4.学习Web API可以结合前面学习内置对象方法的思路学习

## 一、DOM

文档对象模型(Document Object Model，简称DOM)，是W3C组织推荐的处理可扩展标记语言（HTML或者XML)的标准编程接口。
W3C已经定义了一系列的DOM接口，通过这些DOM接口可以改变网页的内容、结构和样式。

### 1.1 DOM树

![image-20220320213151043](D:\学习web\笔记和图片\web学习笔记\img\image-20220320213151043.png)

**文档:**一个页面就是一个文档，DOM中使用document表示

**元素∶**页面中的所有标签都是元素，DOM中使用element表示

**节点∶**网页中的所有内容都是节点（标签、属性、文本、注释等），DOM中使用node表示

**DOM把以上内容都看做是对象**

### 1.2 获取网页元素

根据ID获取
根据标签名获取
通过HTML5新增的方法获取
特殊元素获取

#### 1.根据id获取

consloe.dir();

![image-20220320213818192](D:\学习web\笔记和图片\web学习笔记\img\image-20220320213818192.png)

语法：

```
var element = document.getElementById(id);
```

```html
<div id="time">2022</div>
    <!-- 注意 script这时要写在下面 -->
    <script>
        var timer = document.getElementById('time');
        console.log(timer);
        console.dir(timer);
    </script>
```

#### 2.根据标签名获取

```
var lis = document.getElementsByTagName('li');
//返回的是获取过来元素对象的集合以伪数组的形式存储的，无论里面有没有元素
```

还可以获取某个元素(父元素)内部所有指定标签名的子元素.

```
element.getElementsByTagName ( '标签名");
```

注意∶父元素必须是单个对象(必须指明是哪一个元素对象).获取的时候不包括父元素自己(如下）。

```
//(1)
        var ol = document.getElementsByTagName('ol');
        console.log(ol[0].getElementsByTagName('li'));
//(2)
        var ol = document.getElementById('oli');
        console.log(ol.getElementsByTagName('li'));
```

#### 3.通过HTML5新增的方法获取

##### 1.根据类名getElementsByClassName

不需要加./#

```
var boxs = document.getElementsByClassName('box');
```

##### 2.querySelector

返回指定选择器的第一个元素对象   切记里面的选择器需要加符号 .box/ #nav

```
var firstbox = document.querySelector('.box');
        var nav = document.querySelector('#nav');
```

##### 3.querySelectorAll()

返回指定选择器的所有元素对象集合

```
var all = document.querySelectorAll('.box');
```

#### 4.特殊元素获取(document,html)

![image-20220320221943624](D:\学习web\笔记和图片\web学习笔记\img\image-20220320221943624.png)

### 1.3事件

#### 基础

JavaScript使我们有能力创建动态页面，而事件是可以被JavaScript侦测到的行为。简单理解∶**触发---响应机制**。
网页中的每个元素都可以产生某些可以触发JavaScript的事件，例如，我们可以在用户点击某按钮时产生一个事件，然后去执行某些操作。

事件是有三部分组成事件源﹑事件类型︰事件处理程序―我们也称为事件三要素

//(1）事件源  事件被触发的对象  谁   按钮

//(2）事件类型如何触发什么事件比如鼠标点击(onclick)还是鼠标经过还是键盘按下

//(3)事件处理程序通过一个函数赋值的方式完成

![image-20220320222851234](D:\学习web\笔记和图片\web学习笔记\img\image-20220320222851234.png)

##### 执行事件的步骤

1.获取事件源
2.注册事件（绑定事件)
3.添加事件处理程序(采取函数赋值形式)

##### 常见鼠标事件

![image-20220320223034567](D:\学习web\笔记和图片\web学习笔记\img\image-20220320223034567.png)

#### 高级

##### 1.注册事件（绑定事件)

给元素添加事件，称为注册事件或者绑定事件。注册事件有两种方式∶**传统方式**和**方法监听注册方式**

![image-20220323181140272](D:\学习web\笔记和图片\web学习笔记\img\image-20220323181140272.png)

###### 1.addEventListener 事件监听方式

```
eventTarget.addEventListener(type,listener[,useCapture]) 
//type记得加引号''
```

eventTarget.addEventListener()方法将指定的监听器注册到eventTarget(目标对象）上，当该对象触发指定的事件时，就会执行事件处理函数。

该方法接收三个参数︰
**type**:事件类型字符串，比如click、mouseover，注意这里不要带on
**listener**:事件处理函数，事件发生时，会调用该监听函数
**useCapture** :可选参数，是一个布尔值，默认是false（冒泡阶段）；如果为true，则为**捕获阶段**（见事件流）

```
<button>
        hi
    </button>
    <script>
        var btn = document.querySelector('button');
        btn.addEventListener('click', function () {
            alert('hi');
        })
    </script>
    
```

(1）里面的事件类型是字符串必定加引号而且不带on
(2）同一个元素同一个事件可以添加多个侦听器（事件处理程序)

###### 2. attachEvent事件监听方式(ie9以前支持)

```
eventTarget.attachEvent (eventNameWithon，callback)
```

eventTarget.attachEvent ()方法将指定的监听器注册到eventTarget(目标对象）上，当该对象触发指定的事件时，指定的回调函数就会被执行。

该方法接收两个参数︰
**eventNameWithOn**:事件类型字符串，比如onclick、onmouseover ，这里要带on

**callback**:事件处理函数，当目标触发事件时回调函数被调用

![image-20220323182503691](D:\学习web\笔记和图片\web学习笔记\img\image-20220323182503691.png)

##### 2.删除事件（解绑事件)

1.**传统注册方式**

```
eventTarget.onclick = null;
```

**2.方法监听注册方式**

```
eventTarget.removeEventListener(type，listener[, usecapture] ) ;

eventTarget.detachEvent(eventNamewithon,callback);
```

![image-20220323212341559](D:\学习web\笔记和图片\web学习笔记\img\image-20220323212341559.png)

![image-20220323212416494](D:\学习web\笔记和图片\web学习笔记\img\image-20220323212416494.png)

![image-20220323212433217](D:\学习web\笔记和图片\web学习笔记\img\image-20220323212433217.png)

##### 3.DOM事件流

事件流描述的是从页面中接收事件的顺序。
事件发生时会在元素节点之间按照特定的顺序传播，这个传播过程即DOM事件流。比如我们给一个div注册了点击事件:
**DOM事件流分为3个阶段∶**
1.捕获阶段
2.当前目标阶段
3.冒泡阶段
**事件冒泡**:IE最早提出，事件开始时由最具体的元素接收，然后逐级向上传播到到DOM最顶层节点的过程。
**事件捕获**∶网景最早提出，由DOM最顶层节点开始，然后逐级向下传播到到最具体的元素接收的过程。

<img src="D:\学习web\笔记和图片\web学习笔记\img\image-20220323212854591.png" alt="image-20220323212854591" style="zoom: 80%;" />

事件发生时会在元素节点之间按照特定的顺序传播，这个传播过程即**DOM事件流**。
注意：

1. Js代码中只能执行捕获或者冒泡其中的一个阶段。
2. onclick 和attachEvent只能得到冒泡阶段。
3. addEventListener(type，listener[,useCapture])第三个参数如果是true，表示在事件捕
   获阶段调用事件处理程序;如果是 false (不写默认就是false )，表示在事件冒泡阶段调用事件处理程序。
4. 实际开发中我们很少使用事件捕获，我们更关注事件冒泡。
5. 有些事件是没有冒泡的，比如onblur、onfocus、onmouseenter、onmouseleave

##### 4.事件对象

![image-20220323214706880](D:\学习web\笔记和图片\web学习笔记\img\image-20220323214706880.png)

1.event 就是一个事件对象写到我们侦听函数的小括号里面当形参来看
 2．事件对象只有有了事件才会存在，它是系统给我们自动创建的，不需要我们传递参数
3．事件对象是我们事件的一系列相关数据的集合跟事件相关的比如鼠标点击里面就包含了鼠标的相关信息，鼠标坐标啊，如果是键盘事件里面就包含的键盘事件的信息比如判断用户按下了那个键
 4．这个事件对象我们可以自己命名比如 event . evt、e
5．事件对象也有兼容性问题ie678通过 window.event兼容性的写法e = e  window.event;
![image-20220323214619432](D:\学习web\笔记和图片\web学习笔记\img\image-20220323214619432.png)

###### 事件对象常见属性和方法

![image-20220323214808461](D:\学习web\笔记和图片\web学习笔记\img\image-20220323214808461.png)

注意：

1.e.target 与 this返回的比较相像，但是有所不同：

e.target返回的是触发事件的对象（元素) ， this返回的是绑定事件的对象（元素)
区别:

e.target点击了那个元素，就返回那个元素 this那个元素绑定了这个点击事件，那么就返回谁

2.阻止事件默认行为

可以用return false; 没有兼容性问题（下图）

![image-20220323215820547](D:\学习web\笔记和图片\web学习笔记\img\image-20220323215820547.png)

##### 5.阻止事件冒泡

**标准写法**︰利用事件对象里面的stopPropagation()方法
e.stopPropagation ()
**非标准写法**:IE6-8利用事件对象cancelBubble属性

![image-20220323220151798](D:\学习web\笔记和图片\web学习笔记\img\image-20220323220151798.png)

![image-20220323220227262](D:\学习web\笔记和图片\web学习笔记\img\image-20220323220227262.png)

##### 6.事件委托(代理、委派)

**事件委托的原理**
不是每个子节点单独设置事件监听器，而是事件监听器设置在其父节点上，然后利用冒泡原理影响设置每个子节点。

**事件委托的作用**
我们只操作了一次DOM，提高了程序的性能。

##### 6.常用的鼠标事件MouseEvent

鼠标移动事件：mousemove

![image-20220323221205984](D:\学习web\笔记和图片\web学习笔记\img\image-20220323221205984.png)

![image-20220323221437192](D:\学习web\笔记和图片\web学习笔记\img\image-20220323221437192.png)

##### 7.常用的键盘事件KeyCode

![image-20220323223049176](D:\学习web\笔记和图片\web学习笔记\img\image-20220323223049176.png)

![image-20220323223240553](D:\学习web\笔记和图片\web学习笔记\img\image-20220323223240553.png)

三个时间的执行顺序：down press up

![image-20220323225923090](D:\学习web\笔记和图片\web学习笔记\img\image-20220323225923090.png)

注意：

keyup和keydown不区分字母大小写，keypress区分大小写

注意（京东快递查询放大字体显示案例）:

keydown和keypress在文本框里面的特点∶他们两个事件触发的时候，文字还没有落入文本框中。
keyup事件触发的时候，文字已经落入文本框里面了。

### 1.4操作元素

#### 1.改变元素内容

element.innerText

element.innerHtml

二者都是可读写的，可以获取元素里的内容

区别：

innerText不识别html标签，是非标准的，且回去除空格和换行；

innerHtml识别html标签，时W3C标准，保留空格和换行

![image-20220320235137276](D:\学习web\笔记和图片\web学习笔记\img\image-20220320235137276.png)

#### 2.常用元素的属性操作

图片元素

![image-20220321154216148](D:\学习web\笔记和图片\web学习笔记\img\image-20220321154216148.png)

```
			//注意：img要先声明该变量
			img.src = '../img/ali.png';
            img.title = '阿里';
```

#### 3.表单元素input的属性操作

![image-20220321162507675](D:\学习web\笔记和图片\web学习笔记\img\image-20220321162507675.png)

注意：

修改input内的文字内容时，不可以用innerText（这个适用于普通盒子，如div），而是通过修改value值；

如果想要某个表单被禁用，即button不可以再点击，则用disabled

```
btn.onclick = function () {
            input.value = '点击了';
            this.disabled = true;
            //this指向的是时间函数的调用者
            // btn.disabled = true;
        }
```

#### 4.样式属性操作

我们可以通过S修改元素的大小、颜色、位置等样式。

##### 1.element.style 行内样式操作

如果样式比较少或者功能简单的情况下使用

```
div.onclick = function () {
            this.style.backgroundColor = 'blue';
            this.style.width = '20px';
        }
```

注意：注意:
1.Js 里面的样式采取驼峰命名法比如fontsize、backgroundcolor
2.Js修改style样式操作，产生的是**行内样式**，css权重比较高

##### 2.element.className 类名样式操作

注意︰
1．如果样式修改较多，可以采取操作类名方式更改元素样式。

2.class因为是个保留字，因此使用className来操作元素类名属性3. 3.className会直接更改元素的类名，会覆盖原先的类名。

```html
<div class="first">hhhh</div>
    <script>
        var div = document.querySelector('div');
        div.onclick = function () {
            // div.className = 'change';
            // 如果想要保留原来的样式 多类名选择器
            div.className = 'first change';
        }
    </script>
```

#### 5.排他思想

```html
<script>
        var btn = document.querySelectorAll('button');
        for (var i = 0; i < btn.length; i++) {
            btn[i].onclick = function () {
                //先将其他btn清除背景
                for (var i = 0; i < btn.length; i++) {
                    btn[i].style.backgroundColor = '';
                }
                //再将自己的背景改变
                this.style.backgroundColor = 'pink';
            }
        }
    </script>
```

#### 6.自定义属性的操作

##### 1.获取属性值getAttribute

```html
<div id="demo"></div>
    <script>
        var div = document.querySelector('div');
        // (1)element.属性
        console.log(div.id);
        //(2)element.getAttribute('属性')
        console.log(div.getAttribute('id'));
    </script>
```

区别：

element.属性：获取内置属性值(元素本身自带的属性)
element.getAttribute('属性')：主要获得自定义的属性（标准）我们程序员自定义的属性

##### 2.设置属性值setAttribute

```html
<script>
//(1)element.属性
        div.id = 'd';
        div.className = 'navs';
        // (2)element.getAttribute('属性','属性名')
        div.setAttribute('index', 2);
        div.setAttribute('class', 'footer');
        //注意class属性的设置，两者不太相同
    </script>
```

##### 3.移除属性

```html
<script>
	div.removeAttribute('index');
    </script>
```

##### 4.tab栏切换案例：

![image-20220321235547367](D:\学习web\笔记和图片\web学习笔记\img\image-20220321235547367.png)

位置：D:\学习web\DemoPro\js0321\tab栏切换.html

#### 7.H5自定义属性（有兼容性问题）

自定义属性目的∶是为了保存并使用数据。有些数据可以保存到页面中而不用保存到数据库中。

通过getAttribute('属性')

##### 1.设置H5自定义属性

![image-20220322210930243](D:\学习web\笔记和图片\web学习笔记\img\image-20220322210930243.png)

![image-20220322211015391](D:\学习web\笔记和图片\web学习笔记\img\image-20220322211015391.png)

##### 2.获取属性

![image-20220322211241833](D:\学习web\笔记和图片\web学习笔记\img\image-20220322211241833.png)

![image-20220322211259130](D:\学习web\笔记和图片\web学习笔记\img\image-20220322211259130.png)

![image-20220322211352618](D:\学习web\笔记和图片\web学习笔记\img\image-20220322211352618.png)

### 1.5 节点操作

#### 1.节点概述

网页中的所有内容都是节点(标签、属性、文本、注释等），在DOM中，节点使用node来表示。
HTML DOM树中的所有节点均可通过JavaScript进行访问，所有HTML元素(节点)均可被修改，也可以创建或删除。

![image-20220322212003832](D:\学习web\笔记和图片\web学习笔记\img\image-20220322212003832.png)
一般地，节点至少拥有nodeType(节点类型) 、nodeName(节点名称）和nodeValue(节点值)这三个基本属性。
元素节点nodeType 为1
属性节点nodeType为2
文本节点nodeType 为3(文本节点包含文字、空格、换行等)

#### 2.节点层级

利用DOM树可以把节点划分为不同的层级关系，常见的是父子兄层级关系。

![image-20220322212157966](D:\学习web\笔记和图片\web学习笔记\img\image-20220322212157966.png)

##### 1.父级节点

```
node.parentNode
得到的是元素最近的节点，如果找不到，则会返回null
```

##### 2.子级节点

```
parentNode.childNodes(标准)
返回包含指定节点的子节点的集合，该集合为即时更新的集合。
```

![image-20220322213559841](D:\学习web\笔记和图片\web学习笔记\img\image-20220322213559841.png)

```
parentNode.children(非标准)
parentNode.children是一个只读属性，返回所有的子元素节点。它只返回子元素节点，其余节点不返回（重点掌握）。
```

```
parentNode.firstChild 返回第一个子节点（可能是文本节点）
parentNode.lastChild 返回最后一个子节点（可能是文本节点）
parentNode.firstElementChild 返回第一个子节点，找不到返回null，有兼容性问题，ie9
parentNode.lastElementChild 返回最后一个子节点，找不到返回null，有兼容性问题，ie9
```

```
实际开发中：
parentNode.children[0] 第一个
parentNode.children[parentNode.children.length - 1] 最后一个
```

##### 3.兄弟节点

```
1.node.nextSibling
返回当前元素的下一个兄弟节点，找不到则返回null。同样，也是包含所有的节点。
2. node.previousSibling
返回当前元素上一个兄弟节点，找不到则返回null。同样，也是包含所有的节点。
3. node .nextElementSibling
返回当前元素下一个兄弟元素节点，找不到则返回null。有兼容性问题，ie9
3. node .previousElementSibling
返回当前元素上一个兄弟元素节点，找不到则返回null。有兼容性问题，ie9
```

![image-20220322221654259](D:\学习web\笔记和图片\web学习笔记\img\image-20220322221654259.png)

##### 4.创建节点

```
document.createElement ( 'tagName ' )
```

document.createElement()方法创建由tagName指定的HTML元素。因为这些元素原先不存在，是根据我们的需求动态生成的，所以我们也称为动态创建元素节点。

##### 5.添加节点

```
1.node.appendChild(child)
```

node.appendChild()方法将一个节点添加倒指定父节点的子节点列表末尾。类似于css里面的after伪元素。后面追加元素（相当于push）

```
2. node.insertBefore (child，指定元素)
```

##### 6.删除节点

```
node. removeChild(child)
```

node.removechild()方法从DOM中删除一个子节点，返回删除的节点。

![image-20220322230735869](D:\学习web\笔记和图片\web学习笔记\img\image-20220322230735869.png)

阻止链接跳转需要添加javascript:void(0);或者javascript:;

```
<a href='javascript:'>删除</a>
```

##### 7.复制节点（克隆节点）

```
node.cloneNode()
```

返回调用该方法的节点的一个副本

![image-20220322232833448](D:\学习web\笔记和图片\web学习笔记\img\image-20220322232833448.png)

##### 8.动态生成表格

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        table {
            width: 500px;
            margin: 100px auto;
            border-collapse: collapse;
            text-align: center;
        }

        td,
        th {
            border: 1px solid #333;
        }

        thead tr {
            height: 40px;
            background-color: #ccc;
        }
    </style>
</head>

<body>
    <table cellspacing="0">
        <thead>
            <tr>
                <td>姓名</td>
                <td>科目</td>
                <td>成绩</td>
                <td>操作</td>
            </tr>
        </thead>
        <tbody>

        </tbody>
    </table>

    <script>
        //数组里可以存放对象数据
        var datas = [
            {
                name: 'suruan',
                subject: 'JS',
                score: 100
            }, {
                name: 'susu',
                subject: 'JS',
                score: 90
            }, {
                name: 'surou',
                subject: 'JS',
                score: 99
            }
        ];
        //向tbody内创建行，通过数组长度获取人数
        var tbody = document.querySelector('tbody');
        for (var i = 0; i < datas.length; i++) {
            //创建tr
            var tr = document.createElement('tr');
            tbody.appendChild(tr);
            //创建td 取决于对象的属性个数
            for (var k in datas[i]) {
                var td = document.createElement('td');
                td.innerHTML = datas[i][k];//把对象里的属性值赋值给td
                tr.appendChild(td);
            }
            //创建删除单元格
            var td = document.createElement('td');
            td.innerHTML = '<a href="javascript:;">删除</a>';
            tr.appendChild(td);

        }
        //删除
        var as = document.querySelectorAll('a');
        for (var i = 0; i < as.length; i++) {
            as[i].onclick = function () {
                //要删除当前行tr，tr是td的父亲，td是a的父亲，tr是tbody的子元素
                tbody.removeChild(this.parentNode.parentNode);
            }
        }
    </script>
</body>

</html>
```

##### 9.三种动态创建元素的区别

###### document.write ()

```
document.write ('<div>123</div>')
```

缺点：

document.write是直接将内容写入页面的内容流，但是文档流执行完毕，则它会导致页面全部重绘

![image-20220323174802119](D:\学习web\笔记和图片\web学习笔记\img\image-20220323174802119.png)

###### element .innerHTMT和document.createElement ()

###### ![image-20220323175331171](D:\学习web\笔记和图片\web学习笔记\img\image-20220323175331171.png)

![image-20220323175731540](D:\学习web\笔记和图片\web学习笔记\img\image-20220323175731540.png)

innerHTML，是将内容写入某个DOM节点，不会导致页面全部重绘

innerHTML，创建多个元素效率更高（不要拼接字符串，采取数组形式拼接），结构稍微复杂

createElement()创建多个元素效率稍低一点点，但是结构更清晰

总结∶不同浏览器下，innerHTM，效率要比 creatElement高

### 6.DOM重点核心

![image-20220323180044698](D:\学习web\笔记和图片\web学习笔记\img\image-20220323180044698.png)

关于dom操作，我们主要针对于元素的操作。主要有创建、增、删、改、查、属性操作、事件操作。

#### 1.创建

1. document.write
2. innerHTML
3. createElement

#### 2.增

1.appendChild
2.insertBefore

#### 3.删

1.removeChild

#### 4.改

主要修改dom的元素属性，dom元素的内容、属性,表单的值等

1．修改元素属性: src、href、title等

2．修改普通元素内容:innerHTML、innerText

3．修改表单元素: value、type、disabled等

4．修改元素样式: style、className

#### 5.查

主要获取查询dom的元素

1.DOM提供的API方法: getElementByld、getElementsByTagName 古老用法不太推荐

2.H5提供的新方法: querySelector、querySelectorAll提倡

3.利用节点操作获取元素∶父(parentNode)、子(children)、兄(previousElementSibling,nextElementSibling)提倡

#### 6.属性操作

主要针对于自定义属性。
公
1.setAttribute :设置dom的属性值

2.getAttribute:得到dom的属性值

3.removeAttribute移除属性

#### 7.事件操作

给元素注册事件，采取事件源.事件类型=事件处理程序

![image-20220320223034567](D:\学习web\笔记和图片\web学习笔记\img\image-20220320223034567.png)

## 二、BOM浏览器对象模型

### 1.BOM概述

BOM( Browser Object Model )即浏览器对象模型，它提供了独立于内容而与浏览器窗口进行交互的对象，其核心对象是window。
BOM由一系列相关的对象构成，并且每个对象都提供了很多方法与属性。
BOM缺乏标准，JavaScript语法的标准化组织是ECMA，DOM的标准化组织是W3C，BOM最初是Netscape浏览器标准的一部分。

![image-20220325201143269](D:\学习web\笔记和图片\web学习笔记\img\image-20220325201143269.png)

![image-20220325201230610](D:\学习web\笔记和图片\web学习笔记\img\image-20220325201230610.png)

### 2.window对象的常见事件

window对象是浏览器的顶级对象，它具有双重角色。

1.它是JS访问浏览器窗口的一个接口。
2.它是一个全局对象。定义在全局作用域中的变量、函数都会变成window对象的属性和方法。
在调用的时候可以省略window，前面学习的对话框都属于window对象方法，如alert()、prompt()等。

注意: window下的一个特殊属性window.name

#### 2.1窗口加载事件

```
window.onload = function (){}或者
window.addEventListener( "load" ,function(){};
```

**window.onload**：

窗口(页面）**加载事件**,当文档内容完全加载完成会触发该事件(包括图像、脚本文件、CSS文件等),就调用的处理函数。
注意:
1.有了window.onload就可以把.JS代码写到页面元素的上方，因为onload是等页面内容全部加载完毕，再去执行处理函数。

2.window.onload传统注册事件方式只能写一次，如果有多个，会以最后一个window.onload为准。

3.如果使用addEventListener则没有限制。

**DOMContentLoaded**：

```
document.addEventListener( 'DOMContentLoaded' ,function(){ })
```

DOMContentLoaded事件触发时，仅当DOM加载完成，不包括样式表，图片，flash等等。le9以上才支持。
如果页面的图片很多的话,从用户访问到onload触发可能需要较长的时间交互效果就不能实现，必然影响用户的体验，此时用DOMContentLoaded事件比较合适。

**区别**：

load等页面内容全部加载完毕，包含页面dom元素图片 flash css等等。
DOMContentLoaded是DOM加载完毕，不包含图片 falsh css等就可以执行加载速度比load更快一些。

#### 2.2 调整窗口大小事件

```
window. onresize = function() {}
window .addEventListener ("resize" , function () {});
```

window. onresize是调整窗口大小加载事件，当触发时就调用的处理函数。

注意:
1.只要窗口大小发生像素变化，就会触发这个事件。
⒉我们经常利用这个事件完成响应式布局。window.innerWidth当前屏幕的宽度。

#### 2.3定时器

##### 1.setTimeout()定时器

```
window.setTimeout(调用函数，[延迟的毫秒数]);
```

setTimeout()方法用于设置一个定时器，该定时器在定时器到期后执行调用函数。
注意:
1.window可以省略。
⒉.这个调用函数可以直接写函数，或者写函数名或者采取字符串‘函数名0'三种形式。第三种不推荐
3.延迟的毫秒数省略默认是0，如果写，必须是毫秒。
4.因为定时器可能有很多，所以我们经常给定时器赋值一个标识符。

**回调函数callback:**

setTimeout()这个调用函数我们也称为**回调函数callback**

普通函数是按照代码顺序直接调用。
而这个函数，需要等待时间，时间到了才去调用这个函数，因此称为回调函数。
简单理解∶回调，就是回头调用的意思。上一件事干完，再回头再调用这个函数。
element.onclick = function()或者element.addEventListener("click",fn);里面的函数也是回调函数。

##### 2.**停止定时器setTimeout()**

```
window.clearTimeout (timeoutID)
```

clearTimeout()方法取消了先前通过调用setTimeout ()建立的定时器。
注意∶

1.window可以省略。
2.里面的参数就是定时器的**标识符**（var **time** = **setTimeout**(**closed**, 5000);）。

##### 3.setlnterval()定时器

```
window.setInterval (回调函数,[间隔的毫秒数]);
```

setInterval()方法**重复调用**一个函数，每隔这个时间，就去调用一次回调函数。
注意:

window可以省略。
2.这个调用函数可以直接写函数，或者写函数名或者采取字符串'函数名()三种形式。
3.间隔的毫秒数省略默认是0，如果写，必须是毫秒，表示每隔多少毫秒就自动调用这个函数。
4.因为定时器可能有很多，所以我们经常给定时器赋值一个标识符。

**setTimeout和setInterval区别：**

setTimeout

延时时间到了，就去调用这个回调函数，只调用一次就结束了这个定时器

setInterval
每隔这个延时时间，就去调用这个回调函数，会调用很多次，重复调用这个函数

##### 4.停止定时器setInterval()

```
window.clearInterval(intervalID);
```


clearInterval ()方法取消了先前通过调用setInterval()建立的定时器。
注意∶

1.window可以省略。
2.里面的参数就是定时器的标识符。

##### 5.this指向

![image-20220326165650827](D:\学习web\笔记和图片\web学习笔记\img\image-20220326165650827.png)

![image-20220326165709849](D:\学习web\笔记和图片\web学习笔记\img\image-20220326165709849.png)

![image-20220326165721649](D:\学习web\笔记和图片\web学习笔记\img\image-20220326165721649.png)

### 3.JS执行机制

#### 3.1JS是单线程

JavaScript语言的一大特点就是**单线程**，也就是说，同一个时间只能做一件事。这是因为Javascript这门脚本语言诞生的使命所致——JavaScript是为处理页面中用户的交互，以及操作DOM而诞生的。比如我们对某个DOM元素进行添加和删除操作，不能同时进行。应该先进行添加，之后再删除。
单线程就意味着，所有任务需要排队，前一个任务结束，才会执行后一个任务。这样所导致的问题是∶如果JS执行的时间过长，这样就会造成页面的渲染不连贯，导致页面渲染加载阻塞的感觉。

#### 3.2同步和异步

为了解决这个问题，利用多核CPU的计算能力，HTML5提出Web Worker标准，允许JavaScript脚本创建多个线程。于是，JS中出现了**同步和异步**。
**同步**
前一个任务结束后再执行后一个任务，程序的执行顺序与任务的排列顺序是一致的、同步的。比如做饭的同步做法:我们要烧水煮饭，等水开了( 10分钟之后)，再去切菜，炒菜。
**异步**
你在做一件事情时，因为这件事情会花费很长时间，在做这件事的同时，你还可以去处理其他事情。比如做饭的异步做法，我们在烧水的同时，利用这10分钟，去切菜，炒菜。

**本质区别：**

流水线上各个流程的执行顺序不同。

#### 3.3同步任务和异步任务

**同步任务**
同步任务都在主线程上执行，形成一个**执行栈**。

**异步任务**
JS的异步是通过**回调函数**实现的。

一般而言，异步任务有以下三种类型:

1、普通事件，如click、resize等

2、资源加载，如load、error等

3、定时器，包括setlnterval、setTimeout等

![image-20220326170727465](D:\学习web\笔记和图片\web学习笔记\img\image-20220326170727465.png)

#### 3.4 js执行机制

1.先执行执行栈中的同步任务。
⒉.异步任务(回调函数)放入任务队列中。
3.一旦执行栈中的所有同步任务执行完毕，系统就会按次序读取任务队列中的异步任务，于是被读取的异步任务结束等待状态，进入执行栈，开始执行。

**事件循环**：

由于主线程不断的重复获得任务、执行任务、再获取任务、再执行，所以这种机制被称为事件循环（ eventloop ) .

![image-20220326171921155](D:\学习web\笔记和图片\web学习笔记\img\image-20220326171921155.png)

![image-20220326172609138](D:\学习web\笔记和图片\web学习笔记\img\image-20220326172609138.png)

![image-20220326172657138](D:\学习web\笔记和图片\web学习笔记\img\image-20220326172657138.png)

#### 3.5location对象

window对象给我们提供了一个**location属性**用于**获取或设置窗体的URL**，并且可以用于**解析URL**。因为这个属性返回的是一个对象，所以我们将这个属性也称为location对象。

##### **URL**：

**统一资源定位符**(Uniform Resource Locator, URL)是互联网上标准资源的地址。互联网上的每个文件都有一个唯一的URL，它包含的信息指出文件的位置以及浏览器应该怎么处理它。

![image-20220326173211080](D:\学习web\笔记和图片\web学习笔记\img\image-20220326173211080.png)

##### location对象的属性：

href和search

![image-20220326173438264](D:\学习web\笔记和图片\web学习笔记\img\image-20220326173438264.png)

##### location对象的方法：

assign、replace、reload

![image-20220326194830351](D:\学习web\笔记和图片\web学习笔记\img\image-20220326194830351.png)

#### 3.6navigator对象

navigator对象包含有关浏览器的信息，它有很多属性，我们最常用的是userAgent，该属性可以返回由客户机发送服务器的user-agent头部的值。
下面前端代码可以判断用户那个终端打开页面，实现跳转

![image-20220326195639775](D:\学习web\笔记和图片\web学习笔记\img\image-20220326195639775.png)

#### 3.7history对象

![image-20220326195857874](D:\学习web\笔记和图片\web学习笔记\img\image-20220326195857874.png)

history对象一般在实际开发中比较少用，但是会在一些OA办公系统中见到。

## 三、PC端网页特效

### 1.元素偏移量offset系列

offset翻译过来就是偏移量，我们使用offset系列相关属性可以动态的得到该元素的位置(偏移)、大小等。

获得元素距离带有定位父元素的位置
获得元素自身的大小(宽度高度)

注意:返回的数值都不带单位

![image-20220326200255246](D:\学习web\笔记和图片\web学习笔记\img\image-20220326200255246.png)

![image-20220326200720302](D:\学习web\笔记和图片\web学习笔记\img\image-20220326200720302.png)

offset与style区别：

![image-20220326201110553](D:\学习web\笔记和图片\web学习笔记\img\image-20220326201110553.png)

### 2.元素可视区client系列

client翻译过来就是客户端，我们使用client系列的相关属性来获取元素可视区的相关信息。通过client系列的相关属性可以动态的得到该元素的边框大小、元素大小等。

![image-20220327181130951](D:\学习web\笔记和图片\web学习笔记\img\image-20220327181130951.png)

### 3.立即执行函数

不需要调用，立马能够自己执行的函数

创建了一个独立区域，不会存在变量冲突。

语法：

```
(1)  (function() {})();

(2)  (function() {} ());
```

![image-20220327181854976](D:\学习web\笔记和图片\web学习笔记\img\image-20220327181854976.png)

**pageShow事件**：

下面三种情况都会刷新页面都会触发load事件。1. a标签的超链接
2.F5或者刷新按钮（强制刷新)3．前进后退按钮
但是火狐中，有个特点，有个“往返缓存”，这个缓存中不仅保存着页面数据，还保存了DOM和JavaScript的状态;实际上是将整个页面都保存在了内存里。
所以此时后退按钮不能刷新页面。
此时可以使用pageshow事件来触发。，这个事件在页面显示时触发，无论页面是否来自缓存。在重新加载页面中，pageshow会在load事件触发后触发﹔根据事件对象中的persisted来判断是否是缓存中的页面触发的pageshow事件，**注意这个事件给window添加。**

### 4.元素滚动scroll

我们使用scroll系列的相关属性可以动态的得到该元素的大小、滚动距离等。

scroll当内容超出盒子时，获得的是内容（例如文本内容）的大小，而client获得的是盒子的大小。

![image-20220327183447142](D:\学习web\笔记和图片\web学习笔记\img\image-20220327183447142.png)

![image-20220327183858648](D:\学习web\笔记和图片\web学习笔记\img\image-20220327183858648.png)

![image-20220327193831146](D:\学习web\笔记和图片\web学习笔记\img\image-20220327193831146.png)

### 5.对比

![image-20220327194141839](D:\学习web\笔记和图片\web学习笔记\img\image-20220327194141839.png)

他们主要用法︰

1. offset系列经常用于获得元素位置offsetLeft offsetTop
2. client经常用于获取元素大小clientWidth clientHeight
3. scroll经常用于获取滚动距离scrollTop scrollLeft
4. 注意页面滚动的距离通过window.pagexoffset获得

### 6.mouseenter 和mouseover的区别

mouseenter鼠标事件：
当鼠标移动到元素上时就会触发mouseenter事件，类似mouseover

它们两者之间的差别是：
mouseover鼠标经过自身盒子会触发，经过子盒子还会触发。mouseenter 只会经过自身盒子触发

●之所以这样，就是因为mouseenter不会冒泡
跟mouseenter搭配鼠标离开mouseleave同样不会冒泡

### 7.系列动画函数封装

#### 7.1动画实现原理

**核心原理**︰通过定时器setlnterval)不断移动盒子位置。
实现步骤:
1.获得盒子当前位置

2.让盒子在当前位置加上1个移动距离

3.利用定时器不断重复这个操作

4.加一个结束定时器的条件

5.注意此元素需要**添加定位**，才能使用element.style.left

![image-20220327195045559](D:\学习web\笔记和图片\web学习笔记\img\image-20220327195045559.png)

![image-20220327194811774](D:\学习web\笔记和图片\web学习笔记\img\image-20220327194811774.png)

#### 7.2动画函数简单封装

注意函数需要传递2个参数，动画**对象**和移动到的**距离**。

![image-20220327195104868](D:\学习web\笔记和图片\web学习笔记\img\image-20220327195104868.png)

代码优化：

![image-20220327200143885](D:\学习web\笔记和图片\web学习笔记\img\image-20220327200143885.png)

#### 7.3缓动效果原理

缓动动画就是让元素运动速度有所变化，最常见的是让速度慢慢停下来。
思路:
1.让盒子每次移动的距离慢慢变小，速度就会慢慢落下来。

2．核心算法∶**(目标值-现在的位置)/ 10**做为每次移动的距离步长。

3．停止的条件是∶让当前盒子位置等于目标位置就停止定时器。

4.注意：步长值需要取整(Math.ceil上取整)

匀速动画就是盒子是当前的位置+固定的值10
缓动动画就是盒子当前的位置＋变化的值(目标值–现在的位置)/ 10)

#### 7.4动画函数多个目标值之间移动

可以让动画函数从8oo移动到500。
当我们点击按钮时候，判断步长是正值还是负值

1.如果是正值，则步长往大了取整

1.如果是负值，则步长往小了取整

#### 7.5动画函数添加回调函数

**回调函数原理**∶函数可以作为一个参数。将这个函数作为参数传到另一个函数里面，当那个函数执行完之后，再执行传进去的这个函数，这个过程就叫做回调。

# JS高级

## JS基础复习：

![image-20220402145925955](D:\学习web\笔记和图片\web学习笔记\img\image-20220402145925955.png)

![image-20220402153121961](D:\学习web\笔记和图片\web学习笔记\img\image-20220402153121961.png)

![image-20220402152758640](D:\学习web\笔记和图片\web学习笔记\img\image-20220402152758640.png)

![image-20220402152810644](D:\学习web\笔记和图片\web学习笔记\img\image-20220402152810644.png)

实例对象和类型对象：

![image-20220402153524869](D:\学习web\笔记和图片\web学习笔记\img\image-20220402153524869.png)

### 1.undefined与null区别

undefined代表定义了但是未赋值

null表示定义且赋值了，但是赋值为null

### 2.何时给变量赋值为null

*初始赋值,表明将要赋值为对象
*结束前，对象成为垃圾对象(被垃圾回收器回收)

![image-20220402154316901](D:\学习web\笔记和图片\web学习笔记\img\image-20220402154316901.png)

### 3.严格区别变量类型与数据类型?

![image-20220402154806957](D:\学习web\笔记和图片\web学习笔记\img\image-20220402154806957.png)

3这个不太好理解，可以听到最后再看一遍这一小节的视频（js03）。

### 4.不太好理解

![image-20220402161955687](D:\学习web\笔记和图片\web学习笔记\img\image-20220402161955687.png)

![image-20220402162030153](D:\学习web\笔记和图片\web学习笔记\img\image-20220402162030153.png)

![image-20220402161820501](D:\学习web\笔记和图片\web学习笔记\img\image-20220402161820501.png)

### 5.相关问题

#### 5.1

![image-20220402162508639](D:\学习web\笔记和图片\web学习笔记\img\image-20220402162508639.png)

#### 5.2

n个引用变量指向同一个对象，通过一个变量修改对象内部数据，其它所有变量看到的是修改之后的数据

![image-20220402163525573](D:\学习web\笔记和图片\web学习笔记\img\image-20220402163525573.png)

2个引用变量指向同一个对象，让其中一个引用变量指向另一个对象，另一引用变量依然指向前一个对象

![image-20220402164655026](D:\学习web\笔记和图片\web学习笔记\img\image-20220402164655026.png)

#### 5.3传递变量参数

在js 调用函数时传递变量参数时，是值传递还是引用传递？

值传递，但是值可能为基本类型或者地址值（或者理解为：可能为值传递，也可能为引用传递，但是引用传递的的是地址值）

![image-20220402201530222](D:\学习web\笔记和图片\web学习笔记\img\image-20220402201530222.png)

#### 5.4Js引擎如何管理内存

![image-20220402202721996](D:\学习web\笔记和图片\web学习笔记\img\image-20220402202721996.png)

![image-20220402202746216](D:\学习web\笔记和图片\web学习笔记\img\image-20220402202746216.png)

### 6.对象

![image-20220402204124390](D:\学习web\笔记和图片\web学习笔记\img\image-20220402204124390.png)

![image-20220402204205566](D:\学习web\笔记和图片\web学习笔记\img\image-20220402204205566.png)

**什么时候必须使用['属性名']的方式?**

1.属性名包含特殊字符: -  空格

![image-20220402205700473](D:\学习web\笔记和图片\web学习笔记\img\image-20220402205700473.png)

2.变量（属性）名不确定

```
var p = {};
        var propName = 'myAge';
        var value = 18;
        //这种方法会使得p对象的属性名不是myAge而是propName（见图片）
        p.propName = value;
        console.log(p);
		//所以应该用下面这种方法
        p[propName] = value;
        console.log(p);
```

![image-20220402210103256](D:\学习web\笔记和图片\web学习笔记\img\image-20220402210103256.png)

![image-20220402210033507](D:\学习web\笔记和图片\web学习笔记\img\image-20220402210033507.png)

### 7.函数

![image-20220402212249522](D:\学习web\笔记和图片\web学习笔记\img\image-20220402212249522.png)

![image-20220402212302473](D:\学习web\笔记和图片\web学习笔记\img\image-20220402212302473.png)

#### 回调函数

![image-20220402224413458](D:\学习web\笔记和图片\web学习笔记\img\image-20220402224413458.png)

![image-20220402212841826](D:\学习web\笔记和图片\web学习笔记\img\image-20220402212841826.png)

#### IIFE立即调用函数表达式

别名：匿名函数自调用

![image-20220402214052085](D:\学习web\笔记和图片\web学习笔记\img\image-20220402214052085.png)

window.$：把window对象传入这个匿名函数中，并且同时执行这个函数，在页面载入之前就执行

![image-20220402214148091](D:\学习web\笔记和图片\web学习笔记\img\image-20220402214148091.png)

test:test就是返回了一个叫test的东西，这个test是之前定义好的test的函数，只不过同名而已，同名情况下可以省略后面的:test

（这块比较难懂，希望学完再看可以好一点）

#### 函数中的this

![image-20220402215618849](D:\学习web\笔记和图片\web学习笔记\img\image-20220402215618849.png)

![image-20220402215705023](D:\学习web\笔记和图片\web学习笔记\img\image-20220402215705023.png)