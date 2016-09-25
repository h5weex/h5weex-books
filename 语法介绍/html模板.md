# html模板

先看一个`hello world`的模板：

```
<template>
    <container>
        <text>Hello World</text>
    </container>
</template>
```

- 必须是以`<template>`标签来包含你的程序模板；
- 文本必须是在`<text>`标签中，否则不会显示出来；
- 图片必须是在`<image>`标签中，并且通过样式来指定图片的width和height，否则不会显示出来；
- 每一个标签上都是支持直接写style或者定义class的；
- 每一个标签都是支持定义任意的属性，比如我定义一个url的属性: <div url="xxx"></div>；
- 在`script`中获取自定义数据可以通过：`e.target.attr.url`这种形式来获取；

目前weex支持的标签有：

- container : 是一个用于包装其它组件的最基本容器组件
- div : 是container的别名
- scroller : 滚动器，如果子组件的总高度高于其本身，那么所有的子组件都可滚动
- list : 列表功能的核心组件，通过平滑滚动和内存回收提供了更好的用户体验和性能
- cell : 定义了展现在list中的元件的属性和行为
- text : 文本组件，文本必须在改标签中，否则不显示
- image : 图片组件，用于渲染图片，并且它不能包含任何子组件
- input : 输入框组件，不能包含子组件，目前支持类型：`text`,`password`,`url`,`email`,`tel`等
- switch : 用于创造和管理类似iOS样式的On/Off 开关按钮
- slider : 轮播组件用于在一个网页中展示多个图片
- video : 视频播放器组件
- a : 页面链接组件，一般我们直接定义在文本标签上定义点击事件来替代
- web : 在weex页面中加载一个网页，该网页会采用webview来渲染；


欢迎推荐你身边的前端同学一起来关注我们，关注h5weex。

![](https://img.alicdn.com/tps/TB1C36iNpXXXXaLXVXXXXXXXXXX-430-430.jpg_200x200)
