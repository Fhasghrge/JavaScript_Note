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
- JavaScript会把小数点后6个0以上的浮点数转换为科学计数法
- 所有的语言都有浮点数误差，所以不要测试浮点数
- Number.MIN_VALUE Number.MAX_VALUE 能表达大小范围
- Infinity  超过范围的表达方式
- isFinite  判断是否在有效范围之内
- isNaN 判断是否数值
    - 换经过转换看看能不能转换为数值
    - 对象的转换方法：
        - 先调用valueOf()方法，不行在调用toString()
- 数值转换
    - Number()适用于所有数据
    - parseInt(string, num)适用于字符串,第二个参数表示转换的进制
    - parseFloat()只解析十进制
- String
    - 字符串重新赋值会重新创建一个空间把以前的赋值进来，然后把以前的字符串销毁
    - 转换为字符串
        - toString(num)参数表示转换的进制
        - null 和undefined没有同toString()方法，使用String()
        - null转换成"null"
        - undefined转换成"undefined"
