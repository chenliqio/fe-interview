## 一、是什么
viewport是视区窗口，也就是浏览器显示网页的部分，PC端基本就是显示的区域，移动端viewport超过设备显示区域则会产生滚动条。  
layout viewport (布局视口)：  在iOS Safari中定义了一个viewport meta标签，用来创建一个虚拟的布局视口（layout viewport），而这个视口的分辨率接近于PC显示器，Apple将其定义为980px（其他厂商各有不同）。
visual viewport (视觉视口)：这个视口可以简单的认为是手持设备物理屏幕的可视区域。 
ideal viewport(完美视口)：类似于布局视口，但宽度和视觉视口相同，有了完美视口，用户不用缩放和拖动网页就能够很好的进行网页浏览。


## 二、具有的特性
- width	设置layout viewport 的宽度，为一个正整数，或字符串"width-device"
- initial-scale	设置页面的初始缩放值，为一个数字，可以带小数
- minimum-scale	允许用户的最小缩放值，为一个数字，可以带小数
- maximum-scale	允许用户的最大缩放值，为一个数字，可以带小数
- height	设置layout viewport 的高度，这个属性对我们并不重要，很少使用
- user-scalable	是否允许用户进行缩放，值为"no"或"yes", no 代表不允许，yes代表允许
