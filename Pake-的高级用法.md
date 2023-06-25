#### 1. 如何改写样式，如去掉原站广告、不想要的模块、甚至重新设计？

- 使用 `npm run dev` 启动右键打开 `devtools` 调试模式，找到你需要修改的样式名称，先在 `devtools` 里面验证效果。
- 找到 `src-tauri/src/inject/style.js` 中样式位置 `const css = "/* styles */"`，将需要覆盖的样式写入到变量 `css` 中，你可以直接以该文件作为示例。
[示例](https://github.com/tw93/Pake/blob/master/src-tauri/src/inject/style.js)

#### 2. 如何注入 JS 的逻辑，比如实现事件监听，比如说键盘快捷键？

参考 `src-tauri/src/inject/event.js` 中事件监听 `document.addEventListener`，直接编写即可，这里更多是基础前端的技术。

#### 3. 如何进行容器内的事件和 Pake 通信，比如说 Web 的拖拽、滚动、特殊点击传递啥的？

参考 `src-tauri/src/inject/event.js` 中通信代码 `invoke`，写好事件监听，然后将事件以及参数传递出来，然后参考容器接收事件 `invoke_handler`，自己处理即可，更多可以参考 tauri 官方文档。