# JavaScript 简介

-   JavaScript 发明的最初的目的就是提前在客户端对表单数据进行验证，避免多次与服务器进行数据交换

## JavaScript 简史

-   Netscape 公司的 Brendan Eich 为即将发布的 Netscape Navigator2 开发名为 LiveScript 脚本语言，为了尽快发布与 Sun 公司合作，在发布之前临时改名 JavaScript（为了和 Java 绑定炒作），此时为 JavaScript 1.0
-   Netscape 随即在 Netscape Navigator 3 发布 JavaScript1.1，同时微软在 IE3 中也加名为 JScript 的 JavaScript 实现（这里也说明了 JavaScript 在当时的火爆）
-   两个版本的 JavaScript 带来很多问题，此时 JavaScript 的标准化被提上日程
-   1997 年以 JavaScript1.1 为蓝本的建议提交到了 ECMA（欧洲计算机制造商协会），该协会指定 39 号技术委员会（T39)负责标准化此事-----ECMAScript 1 正式发布
-   第二年,ISO/IEC 采用了 ECMAScript 作为标准，为了和国际保持一致，ECMAScript 升级 ECMAScript 2 但是没有任何修改

## JavaScript 实现

-   JavaScript 由三部分组成
    -   ECMAScript
    -   DOM
    -   BOM
-   ECMAScript
    -   ECMAScript 本身与浏览器没有依赖关系，ECMAScript 这些的基础，JavaScript 利用 BOM，DOM 更好的运用在浏览器宿主环境中，其他的宿主环境由 Node 和 Adobe Falsh
    -   ECMAScript 1 只不过在 JavaScript1.1 上进行了小的改动，使得 ECMAScript 支持范围更加广泛
    -   ECMAScript 2 上面已经说过
    -   ECMAScript 3 是真正的修改，涉及（字符出处理，错误定义，数值输出），增加了（正则表达式，新控制语句，try-catch 异常处理机制）
    -   ECMAScript 4 是一次全方面的修改，但是改动幅度过大，以减分歧严重倒是被废弃，取而代之的是同时间的替代方案 ECMAScript 3.1
    -   ECMAScript 5 就是上面所说的 ECMAScript 3.1（新功能包括了原生的 JSON 对象，继承，高级属性，严格模式）
    -   ECMAScript 6 因为是对 JavaScript 高级程序设计（第三版）的笔记，作者写作时 ECMAScript 6 没有发布，这里也不做说明
-   什么是 ECMAScript 兼容：
    -   支持 ECMAScript 描述的“类型，值，对象，属性和函数”
    -   支持 Unicode 字符标准
    -   自填加更多的“类型，值，对象，属性和函数”
    -   支持 ECMAScript 没定义的“程序和正则表达式”
-   Web 兼容（）
    了解这些历史繁杂无趣，之前看到有人发面经说面试官问主流浏览器支持的版本，不如了解这些：
    参考：http://kangax.github.io/compat-table/es6/
    来源与 CSDN
-   文档对象模型（DOM）
    -   针对 XML 但是扩展用于 HTML 的 API，借助 DOM 的 API 开发人员可以简单的删除，添加，替换或修改任意节点
    -   DOM 使得不重新加载页面就可以修改外观和内容
    -   这时 Netscape 和微软在开发时候再次出现分歧，此时 W3C 开始着手 DOM 标准制定
    -   1998 DOM level 1 发布： DOM CORE 以及 DOM HTML: DOM CORE 规定如何映射 HTML 文档，DOM HTML 在 DOM 核心扩展，添加 HTML 对象和方法
    -   DOM2 增加了鼠标和用户界面事件，范围，遍历等，通过对象接口增加了对 CSS 支持
    -   DOM3 引入同一加载和保存文档的方法
    -   注意： DOM 不仅仅在 JavaScript 中实现，对于其他的语言也有自己的 DOM 标准
    -   值得一提的是，Netscape 继承者 Mozilla 团队致力于构建 100%支持 DOM 的浏览器 FireFox
    -   支持 DOM 成为浏览器开发厂商的首要目标
-   浏览器对象模型（BOM）
    -   支持访问和操作浏览器窗口的浏览器对象模型
    -   BOM 的标准在 HTML5 出来之后才正式的被写入规范
    -   一些扩展：
        -   弹出新浏览器窗口功能
        -   移动，缩放，关闭浏览器窗口功能
        -   提供浏览器详细信息的 navigator 对象
        -   浏览器加载页面详细信息的 location 对象
        -   用户显示器分辨率详细信息的 screen 对象
        -   对 cookies 支持
        -   XMLHttpRequest 以及 IE 的 ActiveXObject 自定义对象
-   当前主流浏览器：IE（trident)，Ｆ ireFox(Gecko), Chrome(blink), Safari(webkit), Opera(blink)(都有独立内核，一定的用户量）~~~~开个玩笑：中国的浏览器每个都有庞大的用户量，但是内核好像搞得不乍样，应了那句话：“只要是被封锁的，我们搞得都很好”
