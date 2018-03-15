
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
```js
encodeURI("https://www.baidu.com");
```
编码整个URL
* encodeURIComponent   
编码URL中的参数
```js
'https://www.baidu.com/s?wd=' + encodeURIComponent('美女')
```



> [Deprecated and obsolete features](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Deprecated_and_obsolete_features)   
  []