## 基本概念

#### 本文需要对 JavaScript 又简单基础或者其他语言的基础

### 严格模式

-   定义了一种不同的解析和执行模式
-   `"use strict";`
-   是一个编译指令，为了保证兼容性不破化 ECMAScript3 而创建的语法

### 习惯

-   加分号
-   `if`只跟一条语句也加`{}`

### 关键字和保留字

-   使用关键字做标识符会出现`indentifer Expected`错误
-   未经声明使用的变量出现`ReferenceError`错误

### 数据类型

-   基本数据类型： undefined, null, boolean, number, string
-   复杂数据类型： object
-   操作符`typeof`
    -   注意`function`类型是`object`但是不会返回 object,就是专门为了区分的
    -   `null`会当作对象返回，`null`指向空指针

### Null

-   保存对象的变量最好初始化为 null，但是没有必要初始化一个 undefined

### Number

-   会识别八进制和十六进制
-   JavaScript 会把小数点后 6 个 0 以上的浮点数转换为科学计数法
-   所有的语言都有浮点数误差，所以不要测试浮点数
-   Number.MIN_VALUE Number.MAX_VALUE 能表达大小范围
-   Infinity 超过范围的表达方式
-   isFinite 判断是否在有效范围之内
-   isNaN 判断是否数值
-   数值转换
    -   Number()适用于所有数据
    -   parseInt(string, num)适用于字符串,第二个参数表示转换的进制
    -   parseFloat()只解析十进制
-   String
    -   字符串重新赋值会重新创建一个空间把以前的赋值进来，然后把以前的字符串销毁
    -   转换为字符串
        -   toString(num)参数表示转换的进制
        -   null 和 undefined 没有同 toString()方法，使用 String()
        -   null 转换成"null"
        -   undefined 转换成"undefined"
-   Object
    -   `var 0 = new Object()`不推荐使用没有括号的实例化
    -   属性和方法
        -   constructor
        -   hasOwnProperty(propertyname)检查是否有相应属性
        -   isPrototypeOf()检查传入的对象是否为当前对象的原型
        -   propertyIsEnumerable()检查属性是否可以枚举
        -   toLocaleString()
        -   toString()
        -   valueOf()
-   操作符
    -   在使用操作符之前都会调用对象的 valueOf()/toString()转换一下
    -   ECMAScript 中所有的数值都已 64 位格式存储，但是位运算符不直接操作 64 位，而是转换为 32 位再操作，然后再转换为 64 位
    -   有符号的右移
        -   使用符号位补充所有的空位，而无符号位的右移使用 0 补充
-   `for-in`用来枚举对象的属性
    -   最好带上 var
    -   枚举的顺序不能确定
-   `label`跳转标识语句
-   函数
    -   函数的参数实际是使用数组来实现的，可以通过`arguments`对象来访问
    -   函数参数的特点，只是为了函数定义时提供便利，并不是必须的
    -   传入参数与`argument`中的元素指向同一个位置，是实时同步的
    -   没有重载
        -   不存在同一个函数，重新定义一下，改变一下参数的数量或者类型就可     以改变函数
-   小结
    -   未指定返回值的函数返回的是`undefined`
    -   ECMAScript 没有函数签名的概念
