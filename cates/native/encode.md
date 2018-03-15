
# escape、encodeURI和encodeURIComponent

## escape
不会对下列字符编码 ASCII字母、数字、@*/+ 
针对字符串使用的，不适用于URL。   
**已经废弃，不推荐使用**

## encodeURI
不会对下列字符编码  ASCII字母、数字、~!@#$&*()=:/,;?+'


## encodeURIComponent
不会对下列字符编码 ASCII字母、数字、~!*()'


## 关于使用
* escape:   
 不推荐使用
* encodeURI   
编码整个URL
```js
encodeURI("https://www.baidu.com");
```
* encodeURIComponent   
编码URL中的参数
```js
'https://www.baidu.com/s?wd=' + encodeURIComponent('美女')
```


## base64
base64的编码解码
```js
function utf8_to_b64( str ) {
    return window.btoa(unescape(encodeURIComponent( str )));
}

function b64_to_utf8( str ) {
    return decodeURIComponent(escape(window.atob( str )));
}

// Usage:
utf8_to_b64('✓ à la mode'); // "4pyTIMOgIGxhIG1vZGU="
b64_to_utf8('4pyTIMOgIGxhIG1vZGU='); // "✓ à la mode"
//译者注:在js引擎内部,encodeURIComponent(str)相当于escape(unicodeToUTF8(str))
//所以可以推导出unicodeToUTF8(str)等同于unescape(encodeURIComponent(str))
```



> [Deprecated and obsolete features](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Deprecated_and_obsolete_features)   
  [简单明了区分escape、encodeURI和encodeURIComponent](http://www.cnblogs.com/season-huang/p/3439277.html)
