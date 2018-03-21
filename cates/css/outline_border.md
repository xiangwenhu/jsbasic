# CSS outline属性以及和border属性的区别

浏览器里，当鼠标点击或使用Tab键让一个链接或者一个radio获得焦点的时候，该元素将会被一个轮廓虚线框围绕。这个轮廓虚线框就是 outline 。


outline in IE   
低版本hideFoucs

document有一个有意思的[hasFocus](https://developer.mozilla.org/en-US/docs/Web/API/Document/hasFocus), 用来检查document或者document里面的任意一个元素是否focus. 
The Document.hasFocus() method returns a Boolean value indicating whether the document or any element inside the document has focus. This method can be used to determine whether the active element in a document has focus.   


**outline 与 border 的区别**   
1. outline不占据空间，不影响元素的几何尺寸
2. outline有可能是非矩形的


>[CSS outline属性以及和border属性的区别](http://blog.csdn.net/ssisse/article/details/51376270)   
[CSS outline 属性](http://www.w3school.com.cn/cssref/pr_outline.asp)