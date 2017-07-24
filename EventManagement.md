# WindowManagement

- 事件绑定

`addEventListener()`：监听某个特定元素

`.on(event,selector,handler)`：批量绑定

- 事件取消：

`.off(event,selector,handler)`

`.off(event,selector)`

`.off(event)`

`.off()`

- 事件触发：

`.trigger(element,event,data)`

- 手势事件：
```js
mui.init({
  gestureConfig:{
   tap: true, //默认为true
   doubletap: true, //默认为false
   longtap: true, //默认为false
   swipe: true, //默认为true
   drag: true, //默认为true
   hold:false,//默认为false，不监听
   release:false//默认为false，不监听
  }
});
```
**注意**:`dragstart`、`drag`、`dragend`共用`drag`开关，`swipeleft`、`swiperight`、`swipeup`、`swipedown`共用`swipe`开关

- 事件监听：
`addEventListener()`

- 自定义事件：

  - 监听自定义事件：
  ```js
  window.addEventListener('customEvent',function(event){
  //通过event.detail可获得传递过来的参数内容
  ....
  });
  ```
  
  - 触发自定义事件：
  `.fire(target,event,data)`
  
 **注意**：目标`webview`必须触发`loaded`事件后才能使用自定义事件
