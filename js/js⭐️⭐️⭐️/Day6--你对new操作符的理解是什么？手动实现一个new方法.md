## 一、new操作符
在JS中，new操作符用于创建一个给定构造函数的实例对象。  
```
function Person(name.age){
    this.name = name;
    this.age = age;
}
Person.prototype.say = function(){
    return 'hello,'+this.name
}
var obj = new Person('karen',20);
console.log(obj) //Person{name:"karen",age:20}
obj.say() //  hello,karen
```
由上面的例子可以知道，实例obj可以：
* 访问到 Person 构造函数中的属性；

* 访问到 Person.prototype中的属性；

## 二、new操作符的作用原理

1. 创建一个新的对象obj；  

2. 将对象与构建函数通过原型链连接起来；

3. 将构建函数中的this绑定到新建的对象obj上；

4. 根据构建函数返回类型作判断，如果是原始值则被忽略，如果是返回对象，需要正常处理。

## 三、模拟new

```
//准备一个构造函数
function Person(name,age){
this.name = name;
this.age = age;
}
//在构造函数的原型上添加一个方法
Person.prototype.say = function(){
    return '我是'+this.name,'今年'+this.age
}

//原生new
const per = new Person('karen',18)
console.log(per.name,per.age); // karen , 18
console.log(per.say()); //我是karen,今年18

// 模拟new
说明：new_object(构造函数，构造函数的形参1，形参2...)
function new_object(){

// 1.创建一个对象 
let obj = {};

// 获取一个构造函数
let Constuctor = [].shift.call(arguments);

//链接到原型
obj.__proto__=Constructor.prototype;

//绑定this，执行构造函数
let result = Constructor.apply(obj,arguments);

//确保new出来的是一个对象
return typeof result === 'object'?result:obj;
}

//模拟new
let per1 = new_object(Person,'swk',18);
console.log(per1.name,per1.age); // swk 18
console.log(per1.say());//我是 swk，今年18
```
