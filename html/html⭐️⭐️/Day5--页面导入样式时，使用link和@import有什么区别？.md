## 一、CSS样式的引入方法
1. 内联样式  
是指在html标签的style属性中直接添加css。
```
<h1 style =“color:red;”></h1>
```
这种方法的缺点就是，只能改变当前的标签样式,并且再次修改的时候不方便。

2. 嵌入样式
是指将样式编写到head的style标签中。
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>学习计时</title>
    <style>
    p{
        color:red;
        font-size:12px;
    }
    </style>
</head>

```
优点：通过css中的选择器选中样式，并为其设置样式，方便统一修改，可以重复使用。

缺点：重复使用只能在当前页面，不能跨页面使用。

3. 外部样式表
将css样式写到外部的css文件中，可以link标签引入或者通过@import引入,这样就可以在不同页面中调用同一个样式。
将样式编写到外部css文件中，可以使用到浏览器的缓存机制，从而加快网页加载速度。

* link
```
<head>

    <link rel="stylesheet" href="./style.css">

</head>
```

* @import  是指使用css的方式引入css
```
<style>

@import url(style.css);

</style>

```
## 二、link 和 @import 的区别
1. ink是HTML标签，@import是css提供的。

2. link引入的样式页面加载时同时加载，@import引入的样式需等页面加载完成后再加载。

3. link没有兼容性问题，@import不兼容ie5以下。

4. link可以通过js操作DOM动态引入样式表改变样式，而@import不可以。


