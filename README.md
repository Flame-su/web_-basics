# web_basics
前端基础
## DOM文档加载步骤： 
- 1.解析HTML结构 
- 2.加载外部的脚本和样式文件 
- 3.解析并执行脚本代码 
- 4.执行$(function(){})内对应代码 
- 5.加载图片等二进制资源 
- 6.页面加载完毕，执行window.onload

## 作用域
全局作用域 函数作用域 es6块级作用域
### var 
- 1.可变量提生，可是不能垮函数作用域，这样就导致了闭包的逻辑
- 2.在｛｝中活着for语句中，导致内存泄漏
### let const
- 1.定义块级作用域的暂时性死区x`
- 2.外层作用域别想请求到内层作用域
- 3.不能重复申明
 
let、const不存在变量提升，var存在变量提升
let、const不能重复声明，var可以重复声明
let、const有块级作用域，var没有块级作用域

## js栈和堆
- 1.基本类型：Underfined ,Null, Boolean,Number,String
- 2.引用类型： Object，Array，Date，Function

+ 基本类型：一般代码逻辑，简单变量，结构体都是放在栈中： 值存储在栈中
+ 引用类型：而对象，以及被装箱的数据放在堆中 ：地址指针存贮在栈中，值在堆中
https://www.cnblogs.com/guchengnan/p/9406607.html
`栈，线性结构，后进先出，便于管理。堆，一个混沌，杂乱无章，方便存储和开辟内存空间`

## 浅拷贝和深拷贝
- 浅拷贝，拷贝指针，按照指针寻找堆里面的值：所以对象时相同的	
- 深靠谱，堆里面的值也进行拷贝
https://blog.csdn.net/weixin_39786171/article/details/80699736
https://www.cnblogs.com/guchengnan/p/9406607.html

值传递，引用传值
引用传值：看指针是否改变
https://segmentfault.com/a/1190000011455443
https://www.cnblogs.com/zareb/p/5699571.html

## 对于function函数:
函数实际上就是对象,每个函数都是Function类型的实例,由于函数是对象,因此函数名也是指向函数对象的一个指针,并不会和函数绑定.

## 实例，对象，类－－－－－类是对象的抽象，对象是类的实例

- 类：代表一类东西：人类，犬类
- 实例：代表具体东西：你，哈士奇          哈士奇 ＝  new 狗
- 对象：这个只是形式的，抽象的		对象（实例）＝new 类 ＝》实例化
- new 的过程就是把对象实例化

Js 里面没有类（ES6以前class）的语法，所以类的概念就通过创造一个对象来实现。
`new过以后 实例都是对象，而对象不全是实例。`

## arguments
arguments对象是所有（非箭头）函数中都可用的局部变量。

arguments并不是数组，只是相像而已，除了长度，没有数组的方法，
所以用
 Array.prototype.slice.call(arguments，num)
args = [].slice.call(arguments)
...arguments
 Array.from(arguments)
### 转换成数组
在严格模式下，剩余参数、默认参数和解构赋值参数的存在不会改变 arguments对象的行为
在非严格模式下，不包含剩余参数、默认参数和解构赋值参数，值会被更改

