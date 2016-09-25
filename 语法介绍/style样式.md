# style样式

先看一个`hello world`的模板：

```
<template>
    <container class="wrapper">
        <text style="color:red;font-size:48">Hello World</text>
    </container>
</template>

<style>
.warpper {
    width: 750;
    height: 400;
    background-color: #ffffff;
    padding-left: 18;
    padding-right: 18;
    margin-bottom: 18;
    border-width: 0;
    border-style: solid;
    border-color: #cccccc;
    border-top-width: 1;
    border-bottom-width: 1;
    box-sizing: border-box;
    flex-direction: column;
}
</style>
```

- 有两种方式来定义一个标签的样式；
- 方式1：直接在标签上写`style`，里面和原来普通的样式写法一致；
- 方式2：在标签上定义`class`,里面写的class名，在后面的`<style>`区块中定义；
- weex是基于flexbox布局的，可以先看看flex布局的教程，[点击这里](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)；
- weex内置了响应式的支持，页面的宽度是以`750`来做为标准，自动适配所有手机；
- 所有的宽度和高度的定义不需要带单位，如px，rem等，仅仅写数字即可；

##### 注意的几个坑：

- 背景色一定是要写成：`background-color`，如果只写`background`是不会生效的；
- 背景图是不支持的，因为所有`<image>`标签都会转化成背景图，如果有元素需要用到背景图，请用`<image>`来替代，通过`postion:relative/absolute`来实现；
- border的实现必须分开写，如：`border-width:1px;border-color:#eeeeee;border-style:solid;`；
- 文本text-overflow的实现：

```
<text style="width: 200;lines: 1;text-overflow: ellipsis;">Hello World World World World World</text>
```

##### 目前weex不支持的特性：

- iconfont
- 伪类选择器

##### 一些技巧：

待补充
