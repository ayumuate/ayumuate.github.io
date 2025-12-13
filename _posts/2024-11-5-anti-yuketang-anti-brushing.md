---
title: 取消雨课堂的网页活动状态检测
date: 2024-11-5 23:51:00 +0800
---

使用雨课堂刷学校的水课时，如果你切换到其它网页、窗口，哪怕只是点一下任务栏，网页也会自动为你暂停视频。所以，你可以按照这简单几步，取消这个活全家的机制。

1. 拖动链接 [雨课堂活全家](javascript:vueObj.info.anti_brushing=false) 到收藏夹。
2. 在雨课堂开始观看视频。
3. 点击这个收藏。
4. 把网页放在一边，为所欲为。

## 核心代码

```javascript
vueObj.info.anti_brushing = false;
```

是的，开发者大发慈悲的在全局变量里藏下了这个检测功能的开关，只要把这个属性设置为 `false`， 就可以关闭这个功能。你完全可以把它做成一个油猴脚本，自动的为你关闭检测功能。

不过，它检测的原理仍然不明，不是常见的 `document.visibilityState`、 `document.hidden` 或 `visibilitychange` 事件[^visibility]。网页的 JavaScript 代码经过混淆，所以也不能马上找到检测部分的代码。

[^visibility]: [页面可见性 API - Web API | MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/Page_Visibility_API)

想要进一步省事儿的读者，可以抓包研究它调用的 API， 然后模拟请求，或者用 Selenium 这样的框架自动操作网页播放视频。
