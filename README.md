JS时间戳转换成不同的时间格式
=========================

首先要知道怎么将时间转成时间戳：

```js

// 定义时间对象并转成时间戳
var date = new Date();
var timestamp = date.getTime();

```

> 原始格式

```js

var timestamp = 1506338965; // 这里一定要数字，非数字会报`Invalid Date`
var time = new Date( timestamp );
console.log( time );

```

> 转换成xxxx/xx/xx 下午x:xx:xx格式

```js

var timestamp = 1506338965;
var time  = new Date( timestamp ).toLocaleString();
console.log( time );

```

> 转换成 xxxx-xx-xx 下午x:xx:xx格式

```js

var timestamp = 1506338965;
var time  = new Date( timestamp ).toLocaleString().replace(/\//g, '-');
console.log( time );

```

> 转成其他格式

```js

var timestamp = 1506338965;
var time = new Date( timestamp );
var year = time.getFullYear();
var month = time.getMonth() + 1;
var day = time.getDate();
var hour = time.getHours();
var minute = time.getMinutes();
var second = time.getSeconds();
return '拼装成你想要的格式'； 

```

> 使用到的api，参考MDN文档：

[new Date MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date)

[toLocaleString MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)

[getFullYear MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date/getFullYear)

[getMonth MDN文档](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getMonth)

[getDate MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date/getDate)

[getHours MDN文档](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getHours)

[getMinutes MDN文档](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getMinutes)

[getSeconds MDN文档](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getSeconds)

[replace MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/replace)

参考链接： http://blog.csdn.net/hsany330/article/details/50499133