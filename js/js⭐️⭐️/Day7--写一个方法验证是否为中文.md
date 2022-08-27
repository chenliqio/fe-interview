## 一、正则表达式
用于定义一些字符串的规则。  
1. 计算机根据正则表达式，然后检查字符串是否符合规则，或则提取出符合规则的内容。
2. 正则表达式的方法
* test 用于检查这个字符串是否符合规则，返回值true或者false。

3. 正则表达式是由一些普通字符和元字符构成的，常见的元字符有：  
^&nbsp;表示匹配输入字符串的开始位置。   
+&nbsp;匹配前面的子表达式一次或多次（大于等于1次）。  
$ 匹配输入字符串的结束位置。




## 二、创建方式
1. 创建正则表达式的对象  
语法：  
var 变量 = new RegExp("正则表达式","匹配模式")  
在构造函数中可以传递匹配模式作为第二个参数：  
i 忽略大小写  
g 在全局匹配
```
var reg = new RegExp("a",i)
console.log(reg.test("abc")) //true
```

2. 使用字面量创建正则表达式
语法：  
var 变量 = /正则表达式/匹配模式
```
var reg = /a/i;
console.log(reg.test("abc")) //true
```
|&nbsp;&nbsp;&nbsp; 表示或者  /a|b/，正则表达式中含有a或者b。   
[]&nbsp;&nbsp;&nbsp;也表示或者  
[ab] == /a|b/

## 三、创建一个方法判断是否为中文
```
function isChinese(str){
    const reg = /^[\u4e00-\u9fa5]+$/
    return reg.test(str)
}
isChinese("这是一个好方法") //true

```
Tip:  
使用的Unicode 编码 4e00 和 9fa5 分别表示第一个汉字和最后一个汉字的编码。
