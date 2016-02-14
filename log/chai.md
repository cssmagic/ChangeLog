---
title: "Chai"
label: "change-log"
issue: "#2"
original: "https://github.com/chaijs/chai/releases"
---

## 3.5.0 / 2016-01-28

For `assert` fans: you now have `assert.includeDeepMembers()` which matches `expect().to.include.deep.members()` and `.should.include.deep.members()`!

致 `assert` 用户：你们现在有了 `assert.includeDeepMembers()` 这个方法，它跟 `expect().to.include.deep.members()` 和 `.should.include.deep.members()` 是对应的！

This release also includes a variety of small bugfixes and documentation fixes. Most notably, we are now governed by a Code Of Conduct - which gives Chai contributors (including those who files issues, work on code, or documentation, or even just hang out on our Slack & Gitter channels) safety from harassment and discrimination.

这个版本还包含了一些细微的错误修正，以及文档修正。最重要的是，我们引入了一部《编码准则》作为今后所有行动的纲领。

## 3.4.2 / 2015-11-15

This is a small documentation bug fix release - it adds extra metatags to each public method to allow us to generate the docs easier for the website.

仅仅是少量的文档变更。

## 3.4.1 / 2015-11-07

This is a small documentation bug fix release - it just fixes a couple of issues with the documentation.

仅仅是少量的文档变更。

## 3.4.0 / 2015-10-21

This release improves some confusing error messages, and adds some new assertions. Key points:

这个版本改进了一些令人困惑的错误信息，并增加了一些新的断言方法。主要包括：

* Feature: New assertion: `expect(1).oneOf([1,2,3])` - for asserting that a given value is one of a set.
* 特性：新增的断言方法：`expect(1).oneOf([1,2,3])`——用来断言一个给定值是否属于某个集合。
* Feature: `.include()` (and variants) will now give better error messages for bad object types. Before `expect(undefined).to.include(1)` would say "expected undefined to include 1", now says "object tested must be an array, an object, or a string but undefined given"
* 特性：`.include()`（及其变体）现在将会对错误的对象类型给出更好的错误信息。以前 `expect(undefined).to.include(1)` 会得到 "expected undefined to include 1"，而现在会提示 "object tested must be an array, an object, or a string but undefined given"。
* Feature: `.throw()` (and variants) can now better determine the Error types, for example `expect(foo).to.throw(node_assert.AssertionError)` now works.
* 特性：`.throw()`（及其变体）现在可以更好地确定错误类型，比如 `expect(foo).to.throw(node_assert.AssertionError)` 现在行得通了。
* Feature: `.closeTo` is now aliased as `.approximately`
* 特性：`.closeTo` 现在是 `.approximately` 的别名。
* BugFix: `.empty` changes from 3.3.0 have been reverted, as they caused breaking changes to arrays which manually set keys.
* 错误修正：`.empty` 从 3.3.0 开始引入的变化已经撤消了，因为在处理那些拥有手工设置的键的数组时，那些变化会导致破坏性的变更。

## 3.3.0 / 2015-09-08

This release adds some new assertions and fixes some quite important, long standing bugs. Here are the cliff notes:

这个版本增加了一些新的断言方法，并修正了一些非常重要且长期存在的 bug。简要汇总如下：

* Bugfix: Property assertions that fail now show a stack trace!
* 错误修正：失败的属性断言现在可以显示调用栈追踪信息了。
* Bugfix: If you've used the `frozen`, `sealed` or `extensible` assertions to test primitives (e.g. `expect(1).to.be.frozen`), you may have noticed that in older browsers (ES5) these fail, and in new ones (ES6) they pass. They have now been fixed to consistently pass.
* 错误修正：如果你曾使用 `frozen`、`sealed` 或 `extensible` 断言来测试基本类型（比如 `expect(1).to.be.frozen`），那你可能已经注意到了，在较旧的浏览器（ES5）中，这些断言会失败，而在较新的浏览器（ES6）中，它们会通过。现在已经统一修正为通过。
* The `assert` interface has been given the following new methods, to align better with other interfaces: `assert.isAtMost`, `assert.isAtLeast`, `assert.isNotTrue`, `assert.isNotFalse`.
* `assert` 接口增加了以下新方法，以便与其它两套接口相对应：`assert.isAtMost`、`assert.isAtLeast`、`assert.isNotTrue`、`assert.isNotFalse`。

## 3.2.0 / 2015-07-19

This release fixes a bug with the previous additions in `3.1.0`. `assert.frozen`/`expect().to.be.frozen`/`.should.be.frozen` all accidentally called `Object.isSealed()` instead. Now they correctly call `Object.isFrozen()`.

这个版本修正了 `3.1.0` 引入的新断言方法的 bug。`assert.frozen`/`expect().to.be.frozen`/`.should.be.frozen` 全都一不小心调用了 `Object.isSealed()` 作为底层实现。现在已经修正为 `Object.isFrozen()` 方法。

If you're using these features, please upgrade immediately.

如果你正在使用这些特性，请立即升级。

It also adds aliases for a lot of `assert` methods:

这个版本还为大量的 `assert` 方法增加了别名：

* expect/should..respondTo: respondsTo
* expect/should..satisfy: satisfies
* assert.ok: assert.isOk
* assert.notOk: assert.isNotOk
* assert.extensible: assert.isExtensible
* assert.notExtensible: assert.isNotExtensible
* assert.sealed: assert.isSealed
* assert.notSealed: assert.isNotSealed
* assert.frozen: assert.isFrozen
* assert.notFrozen: assert.isNotFrozen

## 3.1.0 / 2015-07-16

This release adds assertions for extensibility/freezing/sealing on objects:

增加了对象 extensibility/freezing/sealing 的断言方法：

```js
assert.extensible({});
assert.notExtensible(Object.preventExtensions({}));
expect(Object.preventExtensions({})).to.not.be.extensible;
Object.preventExtensions({}).should.not.be.extensible;

assert.notSealed({});
assert.sealed(Object.seal({}));
expect(Object.seal({})).to.be.sealed;
Object.seal({}).should.be.sealed;

assert.notFrozen({});
assert.frozen(Object.freeze({}));
expect(Object.freeze({})).to.be.frozen;
Object.freeze({}).should.be.frozen;
```

It also adds assertions for checking if a number is NaN:

还增加了一些断言方法，用于检查一个数字是否是 NaN：

```js
assert.isNaN(NaN);
assert.isNotNaN(5);
expect(NaN).to.be.NaN;
expect(5).to.not.be.NaN;
NaN.should.be.NaN;
5.should.not.be.NaN;
```

## 3.0.0 / 2015-06-04

This release contains some small breaking changes. Most people are unlikely to notice them - but here are the breaking changes:

这个版本引入了一些破坏性的小更新。绝大多数人可能完全察觉不到，但我们还是要列一下：

* Switched from "Component" builds to "Browserify" builds for Browsers. If you're using RequireJS with Chai, you might notice a change (chai used to be a global, now it won't be - instead you'll have to `require` it).

* 给浏览器用的发布文件从 "Component" 构建版切换到了 "Browserify" 构建版。如果你是通过 RequireJS 来加载 Chai 的，那你可能会注意到这个变化：`chai` 以前是一个全局变量，但现在不是了——你需要通过 `require` 来引用它。

* `.has.property('foo', undefined)` will now specifically test to make sure that the value `'foo'` is actually undefined - before it simply tested that the key existed (but could have a value).

* `.has.property('foo', undefined)` 现在将会进行深入测试，以确保 `'foo'` 的值确实是 undefined——在以前它只是简单地测试这个键是否存在（但可以有值）。

* `.to.be.a('type')` has changed to support more types, including ES6 types such as `'promise'`, `'symbol'`, `'float32array'` etc, this also means using ES6's `Symbol.toStringTag` affects the behaviour `.to.be.a()`. In addition to this, Errors have the type of `'error'`.
* `.to.be.a('type')` 已经更新，以便支持更多类型的判断，其中包括 ES6 的新增类型，比如 `'promise'`、`'symbol'` 和 `'float32array'` 等等。同时这也意味着，对 ES6 的 `Symbol.toStringTag` 的操作将会影响到 `.to.be.a()` 的行为。此外，错误将视为 `'error'` 类型。

* `assert.ifError()` now follows Node's `assert.ifError()` behaviour - in other words, if the first argument is truthy, it'll throw it.
* `assert.ifError()` 现在遵从 Node 的 `assert.ifError()` 行为——也就是说，如果第一个参数是真值，则将被抛出。

* ReleaseNotes.md is no longer maintained, see the [Github Releases Page](https://github.com/chaijs/chai/releases) instead.

* History.md is no longer maintained, see the [Github Commit Log](https://github.com/chaijs/chai/commits/master) instead.
