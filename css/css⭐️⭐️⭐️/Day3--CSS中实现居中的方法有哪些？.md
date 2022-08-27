## 一、水平居中
1. 行内元素
* 在块级父容器中使行内元素水平居中，只需要`text-align:center;` 。 
* 这种方法可以使`inline`/`inline-block`/`inline-table`等元素实现水平居中。

2. 块级元素
* 块级元素实现水平居中，在元素宽度固定的情况下，设置`margin-left`和`margin-right`为`auto`。
* 无论父级容器和块级元素的宽度如何变化，都不会影响块级元素的居中效果。

3. 多个块级元素
实现方式有两种，利用`inline-block`和弹性布局。

* 一行有多个块级元素，设置块级元素的显示类型为`display：inline-block`，此时块级元素转变为行内元素，为父容器设置`text-align`属性，就可以实现水平居中的效果。

* 使用弹性布局，其中`justify-content：center`可以设置在横轴方向上的对齐方式。


## 二、垂直居中

1. 行内元素
   
   单行元素：设置行内元素的高度`height`和`inline-height`相等。  

2. 多行
* 利用表布局的`vertical-align:center`可以实现垂直居中。
* 利用弹性布局`flex-direction:column`属性也可以实现垂直居中。

3. 块级元素

  - 已知元素高度  
  父容器设置相对定位，子元素设置绝对定位，设置子元素距离顶部50%，同时设置其`margin-top`向上偏移元素高度的一半。

  - 未知元素高度
  先将元素定位到容器中心，再利用tansform中的translate属性，向Y轴反向偏移50%`transform:translateY(-50%)`，使元素的中心与父容器的中心重合。

## 三、水平且垂直居中
1. 宽高固定元素

  设定父级容器为相对定位，设定子元素绝对定位的位置 `position: absolute; top: 50%; left: 50%`，最后使用负向 `margin` 实现水平和垂直居中，margin 的值为宽高（具体的宽高需要根据实际情况计算 padding）的一半。

2. 宽高不固定元素

父容器设置相对定位，子元素设置绝对定位`position:absolute,left:50%,right:50%`接着在水平和垂直两个方向都向反向平移宽高的一半`transform:translate(-50%,-50%)`，从而使元素水平垂直居中。

3. 使用弹性布局  
```
.box{
    display: flex;
    justify-content: center;
    align-items: center;
}
```