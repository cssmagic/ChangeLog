---
title: "Zepto"
label: "change-log"
issue: 6
original: "https://github.com/madrobby/zepto/releases"
---

## 1.2.0

On top of [all the bug fixes found in v1.1.7](https://github.com/madrobby/zepto/releases/tag/v1.1.7), this release also brings new features and some slightly backwards-incompatible changes made to ensure better parity with jQuery.

这个版本在 v1.1.7 的基础上，加入了一些新特性和一些轻微的破坏性变更，以便更好地兼容 jQuery 的行为。

Large changes:

较大的变更：

* Eliminate `__proto__` use from codebase.
* [增强] 在代码库中清除对 `__proto__` 的使用。
* Enable AMD-compatible module output. `Zepto` and `$` are still exported to global namespace, even in the case of module loader, to keep compatibility with plugins.
* [增强] 兼容 AMD 模块标准。不过，即使在作为模块加载的情况下，`Zepto` 和 `$` 仍然会导出为全局的命名空间，以保证对插件的兼容性。

New functionality:

新功能：

* Add `$.noop`
* [新增] `$.noop`
* Add `fn.removeProp()`
* [新增] `fn.removeProp()` 方法
* Add `$.isNumeric()`
* [新增] `$.isNumeric()` 方法
* Add `dataFilter` ajax option
* [新增] Ajax 选项 `dataFilter`
* Provide `$.data()` & `$.hasData()` in optional "data" module
* [新增] "data" 模块：提供 `$.data()` 和 `$.hasData()` 方法
* Add Firefox OS detection
* [新增] 对 Firefox OS 的检测

jQuery compatibility:

对 jQuery 的兼容性：

* Stop falling back to reading properties in `fn.attr()`
* [变更] `fn.attr()` 方法在读取标签属性时不再 fallback 到元素属性
* `fn.attr()` now returns `undefined` for non-existing properties instead of `null`
* [变更] `fn.attr()` 在读取不存在的标签属性时返回 `undefined`，而不再是 `null`
* Add document fragment/shadow DOM support
* [新增] 对文档片断和 Shadow DOM 的支持


## 1.1.7

DOM:

* Fix `fn.closest()` on collections of multiple elements
* [修复] `fn.closest()` 在处理多元素集合时的行为
* `text()` returns text from all matching selectors
* [变更] `text()` 返回所有匹配选择符的文本内容
* Fix `offset()` on documentElement
* [修复] `offset()` 在处理 documentElement 时的行为
* Use the standard API for CSS selector matches
* [增强] 在判断元素是否匹配 CSS 选择符时使用标准 API
* `append()` now accepts array of DOM nodes
* [增强] `append()` 现在接受 DOM 节点组成的数组
* Add multi-window support for embedded scripts
* [新增] 为嵌入脚本增加多窗口支持 %%
* Fix `css()` batch setting on non-existing element
* [修复] `css()` 对不存在的元素进行批量设置时的行为
* Convert null/undefined into "" in `fn.val()` for jQuery compatibility
* [变更] 为兼容 jQuery，在 `fn.val()` 中把 null/undefined 转换为 `""`
* Improve detection of array-like objects
* [增强] 对类数组元素的检测

Ajax:

* Fix appending ajax params to URLs that have a hash component
* [修复] 把 Ajax 参数添加到带 hash 的 URL 时的行为
* Add ajax support for receiving binary data
* [新增] 支持接收二进制数据
* Sufficiently randomize JSONP callback names
* [增强] 显著增加 JSONP 回调函数名的随机性
* Fix assigning query params from `data` with explicit JSONP
* [修复] 对于显式 JSONP，从 `data` 分配查询参数时的行为 %%

Cross-browser:

浏览器兼容性：

* Avoid IE10 error by checking if element is in the DOM before calling `getBoundingClientRect`
* [修复] 在调用 `getBoundingClientRect` 时先检查一下元素是否在 DOM 中，以避免在 IE10 下报错
* Added support for pseudo-elements in IE `getComputedStyle` shim
* [新增] 在 IE 的 `getComputedStyle` shim 脚本中增加对伪元素的支持
* Fix use of ajax `xhrFields` on Android 2.3 and Windows Mobile
* [修复] 在 Android 2.3 和 Windows Mobile 系统下 Ajax `xhrFields` 的使用 %%
* Fx: avoid using vendor prefixes if unprefixed is supported
* [增强] "fx" 模块：如果已经支持无前缀属性，则不再使用前缀

Misc.:

其它杂项：

* Fix dasherize bug in fx module
* [修复] "fx" 模块中的 “dasherize bug” %%
* Fix `swipe` event of touch module
* [修复] "touch" 模块中的 `swipe` 事件
* Avoid exception in `doubleTap`
* [修复] 在 `doubleTap` 事件中避免异常抛出 %%
* Accept function as data for `on` event handler
* [增强] 在 `on` 方法中，可接受函数作为 data
* Populate `event.timeStamp` if it's 0 or missing
* [变更] 当 `event.timeStamp` 为 0 或不存在时仍然输出此属性 %%
