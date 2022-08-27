主要分为两大类，隐藏不占位和隐藏占位型
## 一、隐藏不占位
1. display:none
是最常用的元素隐藏方法，不但隐藏，而且不占位，无法响应点击事件。

2. html的hidden属性
```
<div hidden>隐藏</div>
```
此方法会应用浏览器默认样式[hidden] {display: none;}，所以注意不要和display属性同时使用。  

3. position
```
positon:absolute;
z-index:-999px;
```
先让元素脱标，不占用位置，接着使用层级隐藏在其他元素之下。

4. 设置尺寸
```
  height: 0;
  padding: 0;
  overflow: hidden;
```
通过使用最小化其尺寸被隐藏width，height，padding，border-width和/或font-size。还需多设置一个overflow: hidden;以确保内容不会溢出。

## 二、隐藏占位型
1. opacity
```
    opacity:0;
   
```
opacity属性将元素透明度设置为0，占位，并且有点击事件绑定时，可以触发事件。

2. visible:hiddien
让元素隐身，但是仍然占位，此时页面渲染不显示。

3. transform
```
 transform: scale(0);
 或
 transform: translate(-999px, 0);
```
通过transform属性的平移（移动）、缩放、旋转或倾斜元素等方式，来对元素进行一个隐藏。

5. clip-path
```
clip-path: circle(0);
```
clip-path属性会创建一个裁剪区域，用于确定元素的哪些部分可见。使用clip-path: circle(0)可以达到将元素隐藏的效果，无法响应点击事件。
