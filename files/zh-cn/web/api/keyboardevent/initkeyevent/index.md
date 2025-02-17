---
title: KeyboardEvent.initKeyEvent()
slug: Web/API/KeyboardEvent/initKeyEvent
---
{{ ApiRef("DOM Events") }}

> **警告：** 不要再使用这个方法，而是使用 {{domxref("KeyboardEvent.KeyboardEvent", "KeyboardEvent()")}} 构造函数。
>
> 该方法已从 DOM 规范中删除，并且不受任何现代浏览器支持。Firefox 从版本 93 开始默认通过首选项（`dom.keyboardevent.init_key_event.enabled`）隐藏此方法，并计划很快移除它。

{{deprecated_header}}

KeyboardEvent.initKeyEvent 方法用于初始化使用{{domxref("document.createEvent")}}("KeyboardEvent") 创建的事件的值。 以这种方式初始化的事件必须使用{{domxref("document.createEvent")}}("KeyboardEvent") 方法创建。 在调度之前，必须调用 initKeyEvent 来设置事件。

## Syntax

```
event.initKeyEvent (type, bubbles, cancelable, viewArg,
                    ctrlKeyArg, altKeyArg, shiftKeyArg, metaKeyArg,
                    keyCodeArg, charCodeArg)
```

### Parameters

- _`type`_
  - : 是表示事件类型的{{domxref("DOMString")}}。
- _`bubbles`_
  - : 是{{jsxref("Boolean")}}指示事件是否应该通过事件链冒泡（请参阅冒泡）。
- _`cancelable`_
  - : 是{{jsxref("Boolean")}}我指出事件是否可以被取消（见可取消）。
- _`viewArg`_
  - : 指定{{domxref("UIEvent.view")}}; 此值可能为空。
- _`ctrlKeyArg`_

  - : 如果要生成的虚拟键是包含

    <kbd>Ctrl</kbd>

    键的键的组合，则为{{jsxref("Boolean")}}

- _`altKeyArg`_

  - _: `如果要生成的虚拟键是包含`_

    <kbd>Alt</kbd>

    _`键的键的组合，则为{{jsxref("Boolean")}}。`_

- _`shiftKeyArg`_

  - : A {{jsxref("Boolean")}}如果要生成的虚拟键是包含

    <kbd>Shift</kbd>

    键的键组合，则返回 true。

- _`metaKeyArg`_

  - _: `是{{jsxref("Boolean")}}如果要生成的虚拟键是包含`_

    <kbd>Meta</kbd>

    _`键的键的组合，则为 true。`_

- _`keyCodeArg`_
  - : 是一个无符号长整型，表示被按下的键的虚拟键码值，否则为 0.请参阅{{domxref("KeyboardEvent.keyCode")}}以获取键码列表。
- _`charCodeArg`_
  - : 是一个无符号长整型，表示与按下的键相关的 Unicode 字符，否则为 0。

## Example

```
var event = document.createEvent('KeyboardEvent'); // create a key event
// define the event
event.initKeyEvent("keypress",       // typeArg,
                   true,             // canBubbleArg,
                   true,             // cancelableArg,
                   null,             // viewArg,  Specifies UIEvent.view. This value may be null.
                   false,            // ctrlKeyArg,
                   false,            // altKeyArg,
                   false,            // shiftKeyArg,
                   false,            // metaKeyArg,
                    9,               // keyCodeArg,
                    0);              // charCodeArg);

document.getElementById('blah').dispatchEvent(event);
```

## Specification

键盘事件的这种实现基于 DOM 2 事件早期版本中的关键事件规范，后来从该规范中删除。

initKeyEvent 是 DOM Level 3 事件的当前 Gecko 等价物（最初起草并且不推荐使用{{domxref("KeyboardEvent.KeyboardEvent", "KeyboardEvent()")}} {{domxref("Keyboard.initKeyboardEvent()")}}方法与以下参数：

```
typeArg of type DOMString
canBubbleArg of type boolean
cancelableArg of type boolean
viewArg of type views::AbstractView
keyIdentifierArg of type DOMString
keyLocationArg of type unsigned long
modifiersList of type DOMString);
```
