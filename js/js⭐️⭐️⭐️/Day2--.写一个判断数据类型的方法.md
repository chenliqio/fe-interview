## 一、数据类型
数据类型被分为基本类型和引用类型。  
1. 基本类型：  
* String
* Number
* Boolean
* Undefined
* Null
2. 引用类型：
* Object

## 二、判断方法
1. 使用运算符typeof  
语法：typepf 变量  
String 返回 string  
Number 返回 number 
Boolean返回 boolean  
Undefined 返回 undefined
Null 返回 object （因为Null是专门用来表示一个为空的对象）
Object 返回 object

2. 使用Object.property.toString()
```
 const typeOf = (obj)=>{
            return Object.prototype.toString.call(obj).slice(8,-1).toLowerCase();
        }
        console.log(typeOf([]));    //array
        console.log(typeOf({}));    // object
        console.log(typeOf(null)); //null
```
  








## 补充问题
1. 基本数据类型和引用数据类型的区别。  
JS中的变量都保存在栈内存中：  
* 基本数据类型的值直接在栈内存中储存。
* 值与值之间相互独立，修改一个变量不会对其他变量的值有影响。  
JS中对象保存在堆内存，此时变量保存的值是对象在堆内存中的内存地址（对象的引用），当两个变量都保存的同一个对象引用时，一个变量修改属性时，另一个变量的该属性也会改变。
