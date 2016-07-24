# 一个简单的js模板引擎
工作中我们能见到到很多的模板引擎，如vue，angular的双大括号`{{}}`绑定，或者ejs的`<%%>`绑定等。

这里我通过简单等示例，模拟了js模板引擎最基本的功能和思路。
其实思路很简单，拿本例子来说。
1.利用正则匹配dom中的`{{}}`里的内容
```
<p>宝宝{{ date }}</p>
<a href="{{ ask.url }}">{{ ask.content }}</a>
```
2.把匹配到到字符串替换成对应数据中的变量
```
{
        date: '心里苦',
        ask: {
            url: 'http://baike.baidu.com/link?url=fxEGRD8pNCZmi4UeJkjDY-FXmjXXjpiPrtkGE8d6Hr1fYfOUPfGI69QFi1_2ox4tIyeafiHvgbH-PsKtzw0xLc-amo8znEZAL1acIdMF-0jLLYf2jdHkzEXdx8z_b3V-',
            content: '自称宝宝是一种病'
        }
    }
```
3.重新渲染dom树
```
document.querySelector('body').innerHTML = html;
```

