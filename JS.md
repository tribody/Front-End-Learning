# 原生js实现动画原理
## 运动框架实现思路

 1. 速度(改变值left、right、width、height、opacity)
 2. 缓冲运动: 让当前值与目标值差称为速度的变量
 3. 多物体运动: this对象的运用
 4. 任意值运动: 变量抽离
 5. 链式运动: 传入函数对象
 6. 同时运动: 运用json对象遍历

 jquery的animate动画函数就是封装了这样一个过程。

 	注：[慕课网内容](http://www.imooc.com/learn/167)
