---
title: 'Feature-Policy: autoplay'
slug: Web/HTTP/Headers/Feature-Policy/autoplay
---
{{HTTPSidebar}} {{SeeCompatTable}}

The HTTP {{HTTPHeader("Feature-Policy")}} header `autoplay` directive controls whether the current document is allowed to autoplay media requested through the {{domxref("HTMLMediaElement")}} interface. When this policy is enabled and there were no user gestures, the {{domxref("Promise")}} returned by {{domxref("HTMLMediaElement.play()")}} will reject with a `DOMException`. The {{htmlattrxref("autoplay", "audio")}} attribute on {{HTMLElement("audio")}} and {{HTMLElement("video")}} elements will be ignored.

For more details on autoplay and autoplay blocking, see the article [Autoplay guide for media and Web Audio APIs](/en-US/docs/Web/Media/Autoplay_guide).

## 语法

```
Feature-Policy: autoplay <allowlist>;
```

- \<allowlist>
  - : 允许使用此特性的来源（origin）列表。参见 [`Feature-Policy`](/zh-CN/docs/Web/HTTP/Headers/Feature-Policy#语法)。

## 默认策略

[Google Chrome](https://chromestatus.com/feature/5100524789563392) 的默认值是 `'self'`。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{HTTPHeader("Feature-Policy")}} 标头
- [Feature Policy](/zh-CN/docs/Web/HTTP/Feature_Policy)
- [使用 Feature Policy](/zh-CN/docs/Web/HTTP/Feature_Policy/Using_Feature_Policy)
