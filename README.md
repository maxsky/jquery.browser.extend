# $.browser

`$.browser` 属性允许我们检测哪一个 Web 浏览器正在访问网页，通过浏览器本身返回。它包含四个最流行的浏览器类（在 Internet Explorer，Mozilla 和Webkit，和 Opera）以及每个版本信息标志。

可用的标志有：

* webkit（从 jQuery 1.4 开始）
* safari（不建议使用）
* opera
* msie
* mozilla

因为 `$.browser` 使用 `navigator.userAgent` 来确定平台，因此用户可以通过技术手段来修改该值从而欺骗浏览器。避免该问题的最好办法就是使用 `$.support`，`$.support` 属性比 `$.browser` 提供更有效的检测特定功能的支持。

>**Example:** 如果当前使用的浏览器是 Microsoft 的 Internet Explorer，那么下面的语句会返回 true。

```js
$.browser.msie;
```

>**Example:** 若使用的是 WebKit 的浏览器，则弹出提示框 "this is WebKit!"。

```js
if ($.browser.webkit) {
    alert("this is webkit!");
}
```

>**Example:** 为不同的浏览器设置不同的 CSS 属性。

```js
if ($.browser.msie) {
    $("#div ul li").css("display","inline");
} else {
    $("#div ul li").css("display","inline-table");
}
```

---

# $.browser.version

以下是一些典型的结果：

* Internet Explorer: 6.0, 7.0, 8.0
* Mozilla/Firefox/Flock/Camino: 1.7.12, 1.8.1.3, 1.9
* Opera: 10.06, 11.01
* Safari/Webkit: 312.8, 418.9

请注意，IE8 兼容性视要求成为 IE7。

>**Example:** 弹出当前的 IE 版本:

```js
if ($.browser.msie) {
    alert($.browser.version);
}
```
