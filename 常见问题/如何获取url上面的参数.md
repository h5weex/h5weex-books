# 如何获取url上面的参数

- 在.we文件中是没有window等对象，意味着无法通过window.location来获取URL参数的值；
- 好在weex中提供了一个获取配置的方法：`this.$getConfig()`，通过该方法是可以获取URL上的参数，代码如下：

```
/**
 * 获取URL参数
 */
getUrlParam: function (key) {
    var t = this.$getConfig().bundleUrl;
    var reg = new RegExp('[?|&]' + key + '=([^&]+)');
    var match = t.match(reg);
    return match && match[1];
}
```
