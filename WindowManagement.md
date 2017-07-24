# WindowManagement

- 页面初始化

```js
  mui.plusReady(function(){
     console.log("当前页面URL："+plus.webview.currentWebview().getURL());
});
```
mui插件初始化：`mui.init()`

- 创建子页面
```js
mui.init({
    subpages:[{
      url:'list.html',
      id:'list.html',
      styles:{
        top:'45px',//mui标题栏默认高度为45px；
        bottom:'0px'//默认为0px，可不定义；
      }
    }]
  });
```
`plus.webview.create()`

- 打开新页面:
`mui.openWindow()`

- 打开带原生导航头的新页面：
`mui.openWindowWithTitle()`

- 关闭页面：
`mui.back()`

  三种操作会触发页面关闭：
  - 点击包含`mui-action-back`类的控件
  - 在屏幕内向右快速滑动
  - `Android`手机按下`back`按键

- 预加载：

`mui.init()`加载完可能取不到`webview`对象

`mui.preload()`一次只能加载一个

- 快捷生成代码：
`mheader` `mtab` `mbody`

- 需要注意的地方：

  - 固定栏靠前（带有`mui-bar`属性的节点），放在`mui-content`元素之前
  - 一切内容都要包裹在`mui-content`中
