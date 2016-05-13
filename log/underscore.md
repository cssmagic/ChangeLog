---
title: "Underscore"
label: "change-log"
issue: "#4"
original: "http://underscorejs.org/#changelog"
---

> 先吐个槽：这个项目似乎也不符合 SemVer（语义化版本号）的要求。

## 1.8.3

_April 2, 2015_ — [Diff](https://github.com/jashkenas/underscore/compare/1.8.2...1.8.3) — [Docs](https://cdn.rawgit.com/jashkenas/underscore/1.8.3/index.html)

* Adds an `_.create` method, as a slimmed down version of `Object.create`.
* 增加了一个 `_.create` 方法，相当于 `Object.create` 方法的精简版。
* Works around an iOS bug that can improperly cause `isArrayLike` to be JIT-ed. Also fixes a bug when passing `0` to `isArrayLike`.
* 绕过了 iOS 的一个 bug，这个 bug 会错误地导致 `isArrayLike` 被 JIT。同时修复了 `isArrayLike` 在处理 `0` 时的一个 bug。

## 1.8.2

_Feb. 22, 2015_ — [Diff](https://github.com/jashkenas/underscore/compare/1.8.1...1.8.2) — [Docs](https://cdn.rawgit.com/jashkenas/underscore/1.8.2/index.html)

* Restores the previous old-Internet-Explorer edge cases changed in 1.8.1.
* 回滚了 1.8.1 版针对旧版 IE 的边缘情况所作的那个变更。
* Adds a `fromIndex` argument to `_.contains`.
* 为 `_.contains` 增加了一个 `fromIndex` 参数。

## 1.8.1

_Feb. 19, 2015_ — [Diff](https://github.com/jashkenas/underscore/compare/1.8.0...1.8.1) — [Docs](https://cdn.rawgit.com/jashkenas/underscore/1.8.1/index.html)

* Fixes/changes some old-Internet Explorer and related edge case behavior. Test your app with Underscore 1.8.1 in an old IE and let us know how it's doing...
* 尝试修复某些旧版 IE 在某些边缘情况下的行为。请在旧版 IE 下用 Underscore 1.8.1 来测试你的应用，然后向我们反馈实际运行结果……

## 1.8.0

_Feb. 19, 2015_ — [Diff](https://github.com/jashkenas/underscore/compare/1.7.0...1.8.0) — [Docs](https://cdn.rawgit.com/jashkenas/underscore/1.8.0/index.html)

* Added `_.mapObject`, which is similar to `_.map`, but just for the values in your object. (A real crowd pleaser.)
* 增加了 `_.mapObject`，它与 `_.map` 类似，但它用于处理对象中的值。（众望所归有木有？）
* Added `_.allKeys` which returns _all_ the enumerable property names on an object.
* 增加了 `_.allKeys`，它会返回一个对象的**所有**可枚举属性的属性名。
* Reverted a 1.7.0 change where `_.extend` only copied "own" properties. Hopefully this will un-break you — if it breaks you again, I apologize.
* 本来我们决定从 1.7.0 开始让 `_.extend` 只复制对象 “自身” 的属性，但我们又回滚了这个变更。希望这个决定不会搞挂你的应用——如果搞挂了，我们很抱歉。
* Added `_.extendOwn` — a less-useful form of `_.extend` that only copies over "own" properties.
* 增加了 `_.extendOwn`，它是 `_.extend` 的一个不那么常用的形态，它只复制对象 “自身” 的属性。
* Added `_.findIndex` and `_.findLastIndex` functions, which nicely complement their twin-twins `_.indexOf` and `_.lastIndexOf`.
* 增加了 `_.findIndex` 和 `_.findLastIndex`，它们很好地实现了各自的双胞胎方法 `_.indexOf` 和 `_.lastIndexOf`。
* Added an `_.isMatch` predicate function that tells you if an object matches key-value properties. A kissing cousin of `_.isEqual` and `_.matcher`.
* 增加了一个 `_.isMatch` 判断函数，它可以告诉你一个对象是否匹配给定的属性名值对。它的功能和 `_.isEqual` 和 `_.matcher` 极为相似。
* Added an `_.isError` function.
* 增加了一个 `_.isError` 函数。
* Restored the `_.unzip` function as the inverse of `zip`. Flip-flopping. I know.
* 恢复了 1.5.1 中删除的 `_.unzip` 函数，相当于 `zip` 的反相版本。好吧，你们需要来回转换，我明白。
* `_.result` now takes an optional fallback value (or function that provides the fallback value).
* `_.result` 现在接受一个可选的 fallback 值（或者是一个可以提供 fallback 值的函数）。
* Added the `_.propertyOf` function generator as a mirror-world version of `_.property`.
* 增加了 `_.propertyOf` 这个函数生成器，相当于 `_.property` 的镜像版本。
* Deprecated `_.matches`. It's now known by a more harmonious name — `_.matcher`.
* 弃用 `_.matches`。它已经换了一个更和谐的新名字——`_.matcher`。
* Various and diverse code simplifications, changes for improved cross-platform compatibility, and edge case bug fixes.
* 简化代码，提升跨平台兼容性，修复边缘情况下的 bug。

## 1.7.0

_August 26, 2014_ — [Diff](https://github.com/jashkenas/underscore/compare/1.6.0...1.7.0) — [Docs](https://cdn.rawgit.com/jashkenas/underscore/1.7.0/index.html)

* For consistency and speed across browsers, Underscore now ignores native array methods for `forEach`, `map`, `reduce`, `reduceRight`, `filter`, `every`, `some`, `indexOf`, and `lastIndexOf`. "Sparse" arrays are officially dead in Underscore.
* 出于跨浏览器的一致性和性能考虑，Underscore 现在在实现 `forEach`、`map`、`reduce`、`reduceRight`、`filter`、`every`、`some`、`indexOf` 和 `lastIndexOf` 等方法时会忽略原生的数组方法。“稀疏” 数组在 Underscore 中已经正式灭亡。
* Added `_.iteratee` to customize the iterators used by collection functions. Many Underscore methods will take a string argument for easier `_.property`-style lookups, an object for `_.where`-style filtering, or a function as a custom callback.
* 增加了 `_.iteratee` 方法，用于自定义集合函数所需要的迭代函数。现在 Underscore 的很多方法的参数都趋于一致：可以接受一个字符串参数，以便更容易地实现 `_.property` 风格的查询；也可以接受一个对象参数，以实现 `_.where` 风格的过滤操作；还可以接受一个函数参数，作为自定义的回调函数。
* Added `_.before` as a counterpart to `_.after`.
* 增加了 `_.before`，从而与 `_.after` 相呼应。
* Added `_.negate` to invert the truth value of a passed-in predicate.
* 增加了 `_.negate`，它接受一个判断函数，并将其返回值取反。
* Added `_.noop` as a handy empty placeholder function.
* 增加了 `_.noop`，可以很方便地拿它作为占位符函数。
* `_.isEmpty` now works with `arguments` objects.
* `_.isEmpty` 现在可以处理 `arguments` 对象了。
* `_.has` now guards against nullish objects.
* `_.has` 增加了对 “空” 对象的防卫处理。
* `_.omit` can now take an iteratee function.
* `_.omit` 现在可以接受一个迭代函数作为参数了。
* `_.partition` is now called with `index` and `object`.
* `_.partition` 现在不仅可以处理数组，也可以处理对象了。
* `_.matches` creates a shallow clone of your object and only iterates over own properties.
* `_.matches` 会对你的对象生成一个浅拷贝，并且只迭代对象自身的属性。
* Aligning better with the forthcoming ECMA6 `Object.assign`, `_.extend` only iterates over the object's own properties.
* `_.extend` 方法将只迭代对象自身的属性，更好地向未来的 ES6 `Object.assign` 方法靠拢。
* Falsey guards are no longer needed in `_.extend` and `_.defaults`—if the passed in argument isn't a JavaScript object it's just returned.
* 在使用 `_.extend` 和 `_.defaults` 时，不需要操心非法输入的防卫问题了——如果传入的第一个参数不是一个 JS 对象，会直接将其返回。
* Fixed a few edge cases in `_.max` and `_.min` to handle arrays containing `NaN` (like strings or other objects) and `Infinity` and `-Infinity`.
* 修正了 `_.max` 和 `_.min` 的一些边缘情况，可以更好地处理包含 `NaN`（类似于字符串或其它对象）、`Infinity` 和 `-Infinity` 的数组。
* Override base methods like `each` and `some` and they'll be used internally by other Underscore functions too.
* 强化 `each` 和 `some` 这样的基础方法，它们将在 Underscore 内部被其它函数调用。
* The escape functions handle backticks (`` ` ``), to deal with an IE ≤ 8 bug.
* `escape` 转义函数会处理反引号（`` ` ``），以避免 IE8- 下出现问题。
* For consistency, `_.union` and `_.difference` now only work with arrays and not variadic args.
* 出于一致性考虑，`_.union` 和 `_.difference` 现在只能处理数组，而不能处理其它类型的参数。
* `_.memoize` exposes the cache of memoized values as a property on the returned function.
* `_.memoize` 会在返回的函数身上暴露一个 `cache` 属性，这个属性保存了已计算的所有值。
* `_.pick` accepts `iteratee` and `context` arguments for a more advanced callback.
* `_.pick` 可接受 `iteratee` 和 `context` 参数，从而提供了更高级的回调功能。
* Underscore templates no longer accept an initial `data` object. `_.template` always returns a function now.
* Underscore 的模板函数不再接受初始的 `data` 对象。`_.template` 现在总是返回一个函数。
* Optimizations and code cleanup aplenty.
* 大量优化和代码清理。

## 1.6.0

_February 10, 2014_ — [Diff](https://github.com/jashkenas/underscore/compare/1.5.2...1.6.0) — [Docs](https://cdn.rawgit.com/jashkenas/underscore/1.6.0/index.html)

* Underscore now registers itself for AMD (Require.js), Bower and Component, as well as being a CommonJS module and a regular (Java)Script. An ugliness, but perhaps a necessary one.
* Added `_.partition`, a way to split a collection into two lists of results — those that pass and those that fail a particular predicate.
* Added `_.property`, for easy creation of iterators that pull specific properties from objects. Useful in conjunction with other Underscore collection functions.
* Added `_.matches`, a function that will give you a predicate that can be used to tell if a given object matches a list of specified key/value properties.
* Added `_.constant`, as a higher-order `_.identity`.
* Added `_.now`, an optimized way to get a timestamp — used internally to speed up `debounce` and `throttle`.
* The `_.partial` function may now be used to partially apply any of its arguments, by passing `_` wherever you'd like a placeholder variable, to be filled-in later.
* The `_.each` function now returns a reference to the list for chaining.
* The `_.keys` function now returns an empty array for non-objects instead of throwing.
* … and more miscellaneous refactoring.

（译注：1.6 和更低的版本暂不翻译了）
