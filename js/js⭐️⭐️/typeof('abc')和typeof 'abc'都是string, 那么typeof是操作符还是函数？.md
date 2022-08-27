typeof 是操作符，明确定义在MDN当中,作用是对后方表达式的返回做类型定义。
在后面添加括号其实是改变计算优先级，和四则运算中的括号可以等效理解。
简单举例
```
typeof 123 //"number"
typeof 123+'abc'// "numberabc"
typeof(123+'abc') // "string"

```