# script脚本

先看一个`hello world`的实现：

```
<template>
    <container>
        <text>{{myname}}</text>
    </container>
</template>

<script>
module.exports = {
    data: {
        "myname": "hello world"
    },
    methods: {
        render: function(ds) {
            this.myname = ds;
        }
    },
    created: function () {

    },
    ready: function () {

    }
};
</script>
```

- 必须是以`<script>`标签来包含你的脚本；
- 必须把脚本都定义在`module.exports`这个对象中；
- `data`里面是定义的数据对象，可以通过`this.xxx`获取，在模板中是通过`{{xxx}}`来获取；
- `methods`对象中用来定义自己的函数；
- `created`是生命周期函数，这个时候模板还没有被渲染，常用来在这里定义数据的更新和获取；
- `ready`是生命周期函数，这个时候模板被渲染，常用来做一些自己上报等；
