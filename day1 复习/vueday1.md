### template

template标签 模板标签 ?  会解析但不会渲染

### attributes && prop

type checked:  html的标签属性   跟js没关系

在HTML中是没有数据类型的!!!! 

html中对于checked这种属性 写法是 checked = checked



debugger  手动打断点   



attributes:属性节点



html的标签属性:

​		预定义的标签属性: type checked...

​						浏览器会读取预定义标签属性的值  并在浏览器中做出相应的动作

​		自定义标签属性

​						自定义标签属性只有一个功能,用于携带数据



attribute : 对html标签所有属性的抽象

property: 

​		一般我们把dom元素节点的直接属性  我们称之为property

​		property一般用来抽象预定义标签属性

​		property一般分为两类:

​						布尔值 类似checked (重点讨论   因为用户可以操作到)

​						非布尔值 类似type



没动过prop

​		attr  的修改会去同步  prop

动过prop

​		attr的修改不会同步prop   就是设置过propterty  attr的修改就不会改动prop了

prop的修改不回去同步 attr



浏览器在渲染的时候根据的肯定是prop

### css伪类选择器
  nth-child :以child为中心
  例:  @wrap .item:nth-child(1)
        就是指wrap下的第一个名为item的子元素 (必须全部满足)

  nth-of-type : 以type(元素的类型)为中心  

> 在html中,ul的子节点一般只能是li,不然出问题难以解决

### 现在叫  声明的优先级   没有选择器优先级!!!! 

> work-day01-css复习-css3选择器.md