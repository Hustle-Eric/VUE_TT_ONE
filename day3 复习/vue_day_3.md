## css 复习

flex相关   两组核心概念: 容器&项目   主轴&侧轴

容器上的属性 :

项目上的属性: 

flex:1  为简写属性     代表

​											flex-grow:1   

​                                            flex-shrink:1  

​											flex-basis:0%



## BFC  

规则:

  1.内部的Box会在垂直方向，一个接一个地放置。(块级元素独占一行)
  2.BFC的区域不会与float box重叠。(两列布局)
  3.内部的Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠
  4.计算BFC的高度时，浮动元素也参与计算。(清除浮动)

生成条件 :

1. 根元素  
2. float属性不为none
3. position为absolute或fixed  
4. overflow不为visible  
5. display为inline-block, table-cell, table-caption, flex, inline-flex

## 字体图标

iconfont

​	依赖阿里

iconmoon

​	自己拿矢量图生成一套字体图标

## css预处理器

变量

嵌套

混合  (混合相比于继承  更加的灵活  ;   可以传参数 项目中使用的多)

继承(比较高性能   选择器的组合  并不是样式的复制 一些固定不变的公共样式应该要定义继承 )

​		选择器写法: extend(className  all)



## css后置处理器

postcss:  用来对css文件  进行兼容性处理的(基于 can i use 这个特点 )

知道什么用就行

后期有脚手架  一键执行

## ECMAscript

### ES开发  比较重要的两个编程思想

​		函数化编程

​		异步编程: 区分开回调函数的注册 与调用 

​										注册(线程池中的异步线程把回调放到异步队列中去的那个过程)

​										调用(v8引擎最终来执行)

#### ES6 异步的最佳实践

##### 如何生成一个promise实例?

​		new Promise(执行器)                  默认情况下 返回的是一个pending状态的promise

​																当前的promise的状态如何改变 看执行器的执行过程

​																如果执行器函数的第一个参数被调用 当前这个promise会变为成功状态

​																如果执行器函数的第二个参数被调用 当前这个promise会变为失败状态

​																如果执行器函数报错 当前这个promise会变为失败状态

​		promise.then   ; promise.catch

​																promise状态的改变 得看 then 或者 catch的回调执行结果

​																如果返回一个值   promise 成功

​																返回异常   promise  失败

​																返回一个 promise  当前这个promise跟返回的promise状态一样

​		async函数的返回值

​																async同上



#### 如何正确的使用Promise

			1. 执行器内部一定有衣不带吗 且执行的两个参数一定是在一步的函数中调用的
   			2. then中的回调一般都应该返回一个promise



#### async&await

> async&await 01 02 03 三种方式