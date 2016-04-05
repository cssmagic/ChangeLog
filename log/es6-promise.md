---
title: "ES6-Promise"
label: "change-log"
issue: "#3"
original: "https://github.com/stefanpenner/es6-promise/blob/master/CHANGELOG.md"
---

> 先吐个槽：这个项目不符合 SemVer（语义化版本号）的要求。

## 3.2.0

* improve tamper resistence of `Promise.all` `Promise.race` and `Promise.prototype.then` (note, this isn't complete, but addresses an exception when used \w core-js, follow up work will address entirely)
* 提升 `Promise.all`、`Promise.race` 和 `Promise.prototype.then` 等方法对外部篡改的抵抗力（请注意，这个功能还没有做完，目前只能在与 core-js 同时使用时抛出异常以示警告，接下来的版本将会继续完善）
* remove spec incompatible then chaining fast-path
* 移除与规范不兼容的链式快速路径（chaining fast-path）
* add eslint
* 添加 ESLint
* update build deps
* 更新构建依赖

## 3.1.2

* fix node detection issues with NWJS/electron
* 修正在 NWJS/Electron 环境下无法正确探测 Node 环境的问题

## 3.1.0

* improve performance of `Promise.all` when it encounters a non-promise input object input
* 改进 `Promise.all` 接受非 Promise 对象输入时的性能
* `then`/`resolve` tamper protection
* 保护 `then`/`resolve` 方法不被篡改
* reduce AST size of promise constructor, to facilitate more inlining
* 减少 Promise 构造器的 AST 的体积，使之更易于内联
* Update `README.md` with details about PhantomJS requirement for running tests
* 在 `README.md` 中添加关于运行测试所需的 PhantomJS 的信息
* Mangle and compress the minified version
* 通过压缩和混淆来生成压缩版文件

## 3.0.1

* no longer include `dist/test` in npm releases
* 在 npm 包中不再包含 `dist/test` 文件夹。

## 3.0.0

* use `nextTick()` instead of `setImmediate()` to schedule microtasks with node 0.10. Later versions of nodes are not affected as they were already using `nextTick()`. Note that using `nextTick()` might trigger a depreciation warning on 0.10 as described at https://github.com/cujojs/when/issues/410. The reason why `nextTick()` is preferred is that is `setImmediate()` would schedule a macrotask instead of a microtask and might result in a different scheduling. If needed you can revert to the former behavior as follow:

	在 Node 0.10 中使用 `nextTick()` 代替 `setImmediate()` 来调度微任务（macrotask）。更高版本的 Node 不受影响，因为它们已经在用 `nextTick()` 了。请注意使用 `nextTick()` 可能会在 Node 0.10 中触发一个弃用警告，详情参见 https://github.com/cujojs/when/issues/410 。换用 `nextTick()` 的原因在于 `setImmediate()` 会调度宏微任务而不是微任务，可能导致不一样的调度结果。如有必要，你可以通过以下代码来恢复以前的行为：

	```js
	var Promise = require('es6-promise').Promise;
	Promise._setScheduler(setImmediate);
	```

## 2.3.0

* [#121](https://github.com/stefanpenner/es6-promise/issues/121): Ability to override the internal asap implementation
* [#121](https://github.com/stefanpenner/es6-promise/issues/121)：允许覆盖内部的 asap 实现
* [#120](https://github.com/stefanpenner/es6-promise/issues/120): Use an ascii character for an apostrophe, for source maps
* [#120](https://github.com/stefanpenner/es6-promise/issues/120)：用 ASCII 字符来写撇号，对 source map 更有好

## 2.2.0

* [#116](https://github.com/stefanpenner/es6-promise/issues/116): Expose `asap()` and a way to override the scheduling mechanism on Promise
* [#116](https://github.com/stefanpenner/es6-promise/issues/116)：暴露 `asap()` 接口，允许覆盖 Promise 的调度机制
* Lock to v0.2.3 of ember-cli
* 把 ember-cli 锁定在 v0.2.3

## 2.1.1

* Fix [#100](https://github.com/stefanpenner/es6-promise/issues/100) via [#105](https://github.com/stefanpenner/es6-promise/issues/105): tell browserify to ignore vertx require
* 由 [#105](https://github.com/stefanpenner/es6-promise/issues/105) 修复 [#100](https://github.com/stefanpenner/es6-promise/issues/100)：让 Browserify 忽略 vertx require
* Fix [#101](https://github.com/stefanpenner/es6-promise/issues/101) via [#102](https://github.com/stefanpenner/es6-promise/issues/102): "follow thenable state, not own state"
* 由 [#102](https://github.com/stefanpenner/es6-promise/issues/102) 修复 [#101](https://github.com/stefanpenner/es6-promise/issues/101)：遵从 thenable 的状态，而不是自身的状态

## 2.1.0

* ? (see the commit log)

作者偷懒了，没有写变更记录，但其实这里有个坑：从这个版本开始，脚本加载时就会自动打上补丁，不需要手动调用 `.polyfill()` 方法了。这属于行为变更，只升次版本号也是醉了。

## 2.0.0

* re-sync with RSVP. Many large performance improvements and bugfixes.
* 再次同步 RSVP 的代码。大量的性能提升和错误修复。

## 1.0.0

* first subset of RSVP
* 第一版本，从 RSVP 独立出来的一个子集。
