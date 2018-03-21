# Vue VS React

### 数据绑定
* React   
单向数据流   
* Vue    
数据双向绑定   
React 可以随时添加新的 state 成员；Vue 不行，必须定义时准备好顶级成员，而且非顶级成员也必须通过api设置才能是响应式的；这点，react 比较方便 - vue 可以跟踪任何 scope 的状态，包括各级父甚至不相关的，因为vue采用 getter/setter机制；react 默认只能检测本组件的状态变化，比较受限制

### 实现
* React   
Virtual Dom && JSX
* Vue   
Web Component   
Vue也有Virtual Dom  
Vue也支持JSX

### 生态圈
* React完善
* Vue有待完善


### 上手难度
* React相对大
* Vue小

### 错误提示
* React友好
* Vue不够友好


### 迭代和维护
* React友好
* Vue相对会困难   
当工程规模比较大时，如果处理不当，前端的行为将变得难以预测，进而就难以调试和维护了


### 其他
React 函数式编程特征



>[Vue.js与React的全面对比](http://blog.csdn.net/CystalVon/article/details/78428036)