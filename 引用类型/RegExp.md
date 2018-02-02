# RegExp

*字面量：var expression = / pattern / flags*;

*构造函数：var expression = new RegExp(pattern, flags)*

> flags:
> * g: 表示全局模式，应用于所有字符串
> * i: 不区分大小写
> * m: 多行模式，即在到达一行文本末尾时还会继续查找下一行中是否存在模式匹配的项。

``` javascript
// 匹配字符串中所有at的实例。
var parttern1 = /at/g;
// 匹配第一个"bat"或"cat",不区分大小写。
var parttern2 = /[bc]at/i;
// 匹配所有以"at"结尾的3个字符的组合，不区分大小写。
var parttern3 = /.at/gi
// 匹配第一个[bc]at。
var parttern4 = /\[bc\]at/i;
// 匹配所有.at，不区分大小写。
var parttern5 = /\.at/gi;
// 构造函数构造正则表达式
var parttern6 = new RegExp(".at","gi");
```

> *在ECMAScript3中，正则表达式字面量始终会共享同一个RegExp实例，而使用构造函数创建的每一个新的RegExp实例都是一个新的实例。这个问题在ECMAScript5中得到修改。*

