# 重绘和重排

DOM树和样式结构体组合后构建Render树, Render树类似于DOM树，但区别很大，Render树能识别样式，Render树中每个NODE都有自己的style，而且Render树不包含隐藏的节点 (比如display:none的节点，还有head节点)，因为这些节点不会用于呈现，而且不会影响呈现的，所以就不会包含到Render树中。

## 重绘
重绘是一个元素外观的改变所触发的浏览器行为，例如改变visibility、outline、背景色等属性。

* [outline](http://www.w3school.com.cn/cssref/pr_outline.asp)   
* [background-color](http://www.w3school.com.cn/cssref/pr_background-color.asp)   
* [visibility](http://www.w3school.com.cn/cssref/pr_class_visibility.asp)
* [opacity](http://www.w3school.com.cn/cssref/pr_opacity.asp)
* border-color , color

## 重排
重排是更明显的一种改变，可以理解为Render树需要重新计算。
*  DOM元素的几何属性变化   
    高/宽，margin/border/padding等
* DOM树的结构变化
    * 节点的增加、删除，移动等
    * 节点位置
    * 节点内容
* 获取属性   
    * offsetTop、offsetLeft、 offsetWidth、offsetHeight    
    * scrollTops、crollLeft、scrollWidth、scrollHeight   
    * clientTop、clientLeft、clientWidth、clientHeight
    * getComputedStyle() (currentStyle in IE)
* scroll/resize
* CSS3 animations and transitions
* hover, 输入框输入内容等


## 如何减少
1. 改样式属性操作合并，通过切换class | cssText 一次性操作
2. 读写分离
3. position属性设为absolute或fixed，这样此元素就脱离了文档流 或者display:none
4. document.createDocumentFragment | innerHTML
5. 缓存布局信息，便面多次读取 offset, scroll, client ,getComputedStyle等
6. 避免table   
    网上查好多说table耗时
7. 节点克隆
8. 事件委托




>[10 Ways to Minimize Reflows and Improve Performance — SitePoint](https://www.sitepoint.com/10-ways-minimize-reflows-improve-performance/)