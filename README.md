# test

# heelc edit

1. write you note here every day
2. please leave some note when you commit

# feiyuan edit

# BootStrap学习笔记

标签（空格分隔）： 前端 bootstrap

---

##Bootstraps概念
bootstrap是一种前端框架，基于HTM,CSS,JS。用来快速开发web应用程序和网站。
##Bootstrap优点
    1.移动设备优先：框架高寒了贯穿于整个库的移动设备优先的样式
    2.浏览器支持：所有主流浏览器都支持Bootstrap
    3.易上手：只要具备HTML和css基础知识，就可以开始学习Bootstrap
    4.响应式设计：Bootstrap的响应式CSS能够自适应于台式机，平板电脑和手机。
    5.为开发人员创建接口提供了一个简洁统一的解决方案
    6.包含了功能强大的内置组件，易于定制。
    7.提供了基于web的定制。
    8.开源。
##Bootstrap包
    1.基本结构：Bootstrap提供了一个带有网格系统，链接样式，背景的基本结构
    2.CSS:Bootstrap自带以下特性：全局CSS设置，定义基本的HTML元属样式，可扩展的class，一个先进的网络系统。
    3.组件：Bootstrap包含了十几个自定义的jQuery插件，可以直接包含，也可逐个包含这些插件。
    4.定制：可以定制Bootstrap的组件，LESS变量和jQuery插件来得到自己的版本。

##Bootstrap结构

Bootstrap使用了一些HTML5文档类型（Doctype）元素和CSS属性，所以为了正常使用这些，需要在Bootstrap项目开头包含下面代码段
```
    <!DOCTYPE html>
    <html>
    ...
    </html>
```
移动设备优先
Bootstrap3默认的CSS对移动设备友好支持，为了让Bootstrap开发的网站对移动设备友好，确保适当的绘制和触屏缩放，需要在网页的head中添加viewport meta标签
```
<meta name="viewport" content="width=device-width,initial-scale=1.0">
```
width属性控制宽度，如果网站被不同屏幕分辨率的设备浏览，使用device-width可以确保能正确展示。
initial-scale=1.0确保网页家宅时以1:1比例展示，不会有任何缩放。
在移动设备浏览器上，通过为viewport meta 标签添加user-scalable=no 可以禁用其缩放功能。
通常情况下上面两个一起用，用户就只能滚动屏幕，让网站看起来更像原生应用。
```
<meta name = "viewport" content = "width=device-width,
maximum-scale=1.0,
initial-scale-1,0, 
user-scalable=no">
```

##响应式图像
```
<img src = "..." class="img-responsive" alt="响应式图像">
.img-responsive {
  display: block;
  height: auto;
  max-width: 100%;
}
```
在以上代码中，可以看到img-responsive class为图像赋予了max.width:100%和height:auto属性，可以让图像按比例缩放，不超过总尺寸。
这表明相关的图像呈现为 block。当您把元素的 display 属性设置为 block，以块级元素显示。
设置 height:auto，相关元素的高度取决于浏览器。
设置 max-width 为 100% 会重写任何通过 width 属性指定的宽度。这让图片对响应式布局的支持更友好。
如果需要让使用了 .img-responsive 类的图片水平居中，请使用 .center-block 类，不要用 .text-center。