## 一、是什么
函数内部存在两个特殊的对象，arguments和this。  
arguments是一个类数组对象，包含调用函数时传入的所有参数。

## 二、特点
1. 只在以function定义的函数中存在（标准函数）；

2. arguments是类数组对象，不是数组，但是具有数组的length和下标取值，但是有些数组的方法不能用，eg：Array.push()pop()之类的方法；

3. 通常情况下不会对arguments进行操作，会将其转变为数组，方法有三个：
* [...arguments]
* Array.from(arguments)
* [].slice.call(arguments)

4. arguments.callee是函数本身, 严格模式禁用arguments.callee。
