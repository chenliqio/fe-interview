## 一、传统布局
1. 文档流布局
利用display属性，按照文档顺序逐渐显示出来。

2. 浮动布局
利用float属性，使元素脱离文档流，从而浮动起来。

3. 定位布局
利用position属性对元素进行定位。

## 二、flex布局
1. flex布局只适用于ie 10+.  
在 flex 中，最核心的概念就是容器和轴，所有的属性都是围绕容器和轴设置的。其中，容器分为父容器和子容器。轴分为主轴和交叉轴（主轴默认为水平方向，方向向右，交叉轴为主轴顺时针旋转 90°）。
特点：  
* 任何一个容器都可以设置flex布局；
* 行内元素也可以使用flex： inline-flex；
* webkit内核浏览器，必须加上前缀：display: -webkit-flex;
* 设为 flex 布局以后，子元素的float、clear和vertical-align属性将失效。

2. 容器属性
- flex-direction ：决定主轴方向。
- flex-wrap：一条轴线放不下时，决定如何换行。
- flex-flow：前两者的缩写。
- justify-content：定义了项目在主轴方向上的对齐方式。
- align-items：定义项目在交叉轴上如何对齐。
- align-content：定义了多根轴线的对齐方式。

3. 项目属性
- order：定义项目的排列顺序。数值越小，排列越靠前，默认为0。
- flex-grow：定义项目的放大比例，默认为0。
- flex-shrink：定义了项目的缩小比例，默认为1。
- flex-basis：定义了在分配多余空间之前，项目占据的主轴空间。
- flex：属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。
- align-self：允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。


## 三、grid布局
grid 布局又称为“网格布局”，可以实现二维布局方式。  
当一个 HTML 元素将 display 属性设置为 grid 或 inline-grid 后，它就变成了一个网格容器，这个元素的所有直系子元素将成为网格元素。  
grid-template-columns  定义网格行。grid-template-rows 属性来定义网格中列。