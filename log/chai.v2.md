---
title: "Chai (v2)"
label: "change-log"
issue: "#1"
original: "https://github.com/chaijs/chai/blob/master/ReleaseNotes.md"
---

## 2.3.0 / 2015-04-26

Added `ownPropertyDescriptor` assertion:

增加了 `ownPropertyDescriptor` 断言方法：

```js
expect('test').to.have.ownPropertyDescriptor('length');
expect('test').to.have.ownPropertyDescriptor('length', { enumerable: false, configurable: false, writable: false, value: 4 });
expect('test').not.to.have.ownPropertyDescriptor('length', { enumerable: false, configurable: false, writable: false, value: 3 });
expect('test').ownPropertyDescriptor('length').to.have.property('enumerable', false);
expect('test').ownPropertyDescriptor('length').to.have.keys('value');
```

## 2.2.0 / 2015-03-26

Deep property strings can now be escaped using `\\` - for example:

深层属性（deep property）字符串现在可以用 `\\` 来转义了，比如这样：

```js
var deepCss = { '.link': { '[target]': 42 }};
expect(deepCss).to.have.deep.property('\\.link.\\[target\\]', 42)
```

## 2.1.2 / 2015-03-15

A minor bug fix. No new features.

细微的 bug 修复，没有引入新特性。

## 2.1.1 / 2015-03-04

Two minor bugfixes. No new features.

细微的 bug 修复，没有引入新特性。

## 2.1.0 / 2015-02-23

Small release; fixes an issue where the Chai lib was incorrectly reporting the version number.

这是一个小版本：修正了版本号的错误。

Adds new `should.fail()` and `expect.fail()` methods, which are convenience methods to throw Assertion Errors.

增加了 `should.fail()` 和 `expect.fail()`，便于手动抛出断言错误。

## 2.0.0 / 2015-02-09

Unfortunately with 1.10.0 - compatibility broke with older versions because of
the `addChainableNoop`. This change has been reverted.

Any plugins using `addChainableNoop` should cease to do so.

Any developers wishing for this behaviour can use [dirty-chai](https://www.npmjs.com/package/dirty-chai)
by [@joshperry](https://github.com/joshperry)

撤消了 1.10.0 引入的一个破坏性变更。这个版本的变更似乎只对插件开发者有影响，对普通用户没有影响。

## 1.10.0 / 2014-11-10

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required
- **Plugin Developers:**
  - Review `addChainableNoop` notes below.
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

这个版本的变更对普通用户没有影响。

### Noop Function for Terminating Assertion Properties

The following assertions can now also be used in the function-call form:

以下断言方法现在也可以以函数调用的形式来使用：

* ok
* true
* false
* null
* undefined
* exist
* empty
* arguments
* Arguments

The above list of assertions are property getters that assert immediately on access. Because of that, they were written to be used by terminating the assertion chain with a property access.

```js
expect(true).to.be.true;
foo.should.be.ok;
```

This syntax is definitely aesthetically pleasing but, if you are linting your
test code, your linter will complain with an error something like "Expected an
assignment or function call and instead saw an expression." Since the linter
doesn't know about the property getter it assumes this line has no side-effects,
and throws a warning in case you made a mistake.

Squelching these errors is not a good solution as test code is getting to be
just as important as, if not more than, production code. Catching syntactical
errors in tests using static analysis is a great tool to help make sure that your
tests are well-defined and free of typos.

A better option was to provide a function-call form for these assertions so that
the code's intent is more clear and the linters stop complaining about something
looking off. This form is added in addition to the existing property access form
and does not impact existing test code.

```js
expect(true).to.be.true();
foo.should.be.ok();
```

These forms can also be mixed in any way, these are all functionally identical:

```js
expect(true).to.be.true.and.not.false();
expect(true).to.be.true().and.not.false;
expect(true).to.be.true.and.not.false;
```

#### Plugin Authors

If you would like to provide this function-call form for your terminating assertion
properties, there is a new function to register these types of asserts. Instead
of using `addProperty` to register terminating assertions, simply use `addChainableNoop`
instead; the arguments to both are identical. The latter will make the assertion
available in both the attribute and function-call forms and should have no impact
on existing users of your plugin.

（这一段就不翻译了。）

## 1.9.2 / 2014-09-29

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required
- **Plugin Developers:**
  - No changes required
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

这个版本的变更对普通用户没有影响。

## 1.9.1 / 2014-03-19

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - Migrate configuration options to new interface. (see notes)
- **Plugin Developers:**
  - No changes required
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

普通用户在升级到这个版本时，需要阅读以下段落。

### Configuration
### 配置

There have been requests for changes and additions to the configuration mechanisms
and their impact in the Chai architecture. As such, we have decoupled the
configuration from the `Assertion` constructor. This not only allows for centralized
configuration, but will allow us to shift the responsibility from the `Assertion`
constructor to the `assert` interface in future releases.

These changes have been implemented in a non-breaking way, but a depretiation warning will be presented to users until they migrate. The old config method will be removed in either `v1.11.0` or `v2.0.0`, whichever comes first.

旧版的配置方法将在 `v1.11.0` 或 `v2.0.0` 中移除。

#### Quick Migration
#### 快速迁移

```js
// change this:
// 把这种写法：
chai.Assertion.includeStack = true;
chai.Assertion.showDiff = false;

// ... to this:
// 改成这样：
chai.config.includeStack = true;
chai.config.showDiff = false;
```

#### All Config Options
#### 所有配置选项

##### `config.includeStack`

- **@param** _{Boolean}_
- **@default** `false`

User configurable property, influences whether stack trace is included in
Assertion error message. Default of `false` suppresses stack trace in the error
message.

##### `config.showDiff`

- **@param** _{Boolean}_
- **@default** `true`

User configurable property, influences whether or not the `showDiff` flag
should be included in the thrown AssertionErrors. `false` will always be `false`;
`true` will be true when the assertion has requested a diff be shown.

##### `config.truncateThreshold` **(NEW)**

- **@param** _{Number}_
- **@default** `40`

User configurable property, sets length threshold for actual and expected values
in assertion errors. If this threshold is exceeded, the value is truncated.

Set it to zero if you want to disable truncating altogether.

```js
chai.config.truncateThreshold = 0; // disable truncating
```

## 1.9.0 / 2014-01-29

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required
- **Plugin Developers:**
  - Review [#219](https://github.com/chaijs/chai/pull/219).
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

这个版本的变更对普通用户没有影响。

## 1.8.1 / 2013-10-10

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - Refresh `node_modules` folder for updated dependencies.
- **Plugin Developers:**
  - No changes required
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

普通用户在升级到这个版本时，需要更新 `node_modules` 目录以便更新依赖。

### Browserify

This is a small patch that updates the dependency tree so browserify users can install chai. (Remove conditional requires)

稍微更新了一下依赖树（删掉了有条件的 `require` 语句），这样 Browserify 的用户也可以安装 Chai 了。

## 1.8.0 / 2013-09-18

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - See `deep.equal` notes.
- **Plugin Developers:**
  - No changes required
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

普通用户在升级到这个版本时，需要阅读以下 “Deep Equals” 段落。

### Deep Equals
### 深层相等

This version of Chai focused on a overhaul to the deep equal utility. The code for this tool has been removed from the core lib and can now be found at: [chai / deep-eql](https://github.com/chaijs/deep-eql). As stated in previous releases, this is part of a larger initiative to provide transparency, independent testing, and coverage for some of the more complicated internal tools.

For the most part `.deep.equal` will behave the same as it has. However, in order to provide a consistent ruleset across all types being tested, the following changes have been made and _might_ require changes to your tests.

**1.** Strict equality for non-traversable nodes according to [egal](http://wiki.ecmascript.org/doku.php?id=harmony:egal).

**1.** 根据 [egal](http://wiki.ecmascript.org/doku.php?id=harmony:egal) 的描述，不可遍历的节点采用严格对等算法.

_Previously:_ Non-traversable equal via `===`.

*以前的行为*：不可遍历的值通过 `===` 来比较。

（从此版本开始，以下断言将通过。）

```js
expect(NaN).to.deep.equal(NaN);
expect(-0).to.not.deep.equal(+0);
```

**2.** Arguments are not Arrays (and all types must be equal):

**2.** `arguments` 不是数组（所有类型都必须相等）：

_Previously:_ Some crazy nonsense that led to empty arrays deep equaling empty objects deep equaling dates.

*以前的行为*：错误地把空数组、空对象和日期对象视为相等。

（从此版本开始，以下断言将通过。）

```js
expect(arguments).to.not.deep.equal([]);
expect(Array.prototype.slice.call(arguments)).to.deep.equal([]);
```

### CI and Browser Testing

Chai now runs the browser CI suite using [Karma](http://karma-runner.github.io/) directed at [SauceLabs](https://saucelabs.com/). This means we get to know where our browser support stands... and we get a cool badge:

Chai 现在使用 [SauceLabs](https://saucelabs.com/) 上的 [Karma](http://karma-runner.github.io/) 来运行浏览器端的持续集成测试套件。这表示我们可以随时获知浏览器支持情况……而且还顺带收获了一幅漂亮的徽章：

[![Selenium Test Status](https://saucelabs.com/browser-matrix/logicalparadox.svg)](https://saucelabs.com/u/logicalparadox)

Look for the list of browsers/versions to expand over the coming releases.

## 1.7.2 / 2013-06-27

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required.
- **Plugin Developers:**
  - No changes required
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

这个版本的变更对普通用户没有影响。

### Coverage Reporting

Coverage reporting has always been available for core-developers but the data has never been published
for our end users. In our ongoing effort to improve accountability this data will now be published via
the [coveralls.io](https://coveralls.io/) service. A badge has been added to the README and the full report
can be viewed online at the [chai coveralls project](https://coveralls.io/r/chaijs/chai). Furthermore, PRs
will receive automated messages indicating how their PR impacts test coverage. This service is tied to TravisCI.

增加了测试覆盖率报告。

## 1.7.1 / 2013-06-24

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required.
- **Plugin Developers:**
  - No changes required
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

这个版本的变更对普通用户没有影响。

### Official Bower Support

Support has been added for the Bower Package Manager [bower.io](http://bower.io/). Though Chai could be installed via Bower in the past, this update adds official support via the `bower.json` specification file.

正式支持 Bower。

## 1.7.0 / 2013-06-17

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required.
- **Plugin Developers:**
  - Review AssertionError update notice.
- **Core Contributors:**
  - Refresh `node_modules` folder for updated dependencies.

这个版本的变更对普通用户没有影响。

### AssertionError Update Notice

Chai now uses [chaijs/assertion-error](https://github.com/chaijs/assertion-error) instead an internal
constructor. This will allow for further iteration/experimentation of the AssertionError constructor
independant of Chai. Future plans include stack parsing for callsite support.

This update constructor has a different constructor param signature that conforms more with the standard
`Error` object. If your plugin throws and `AssertionError` directly you will need to update your plugin
with the new signature.

```js
var AssertionError = require('chai').AssertionError;

/**
 * previous
 *
 * @param {Object} options
 */

throw new AssertionError({
    message: 'An assertion error occurred'
  , actual: actual
  , expect: expect
  , startStackFunction: arguments.callee
  , showStack: true
});

/**
 * new
 *
 * @param {String} message
 * @param {Object} options
 * @param {Function} start stack function
 */

throw new AssertionError('An assertion error occurred', {
    actual: actual
  , expect: expect
  , showStack: true
}, arguments.callee);

// other signatures
throw new AssertionError('An assertion error occurred');
throw new AssertionError('An assertion error occurred', null, arguments.callee);
```

#### External Dependencies

This is the first non-developement dependency for Chai. As Chai continues to evolve we will begin adding
more; the next will likely be improved type detection and deep equality. With Chai's userbase continually growing
there is an higher need for accountability and documentation. External dependencies will allow us to iterate and
test on features independent from our interfaces.

Note: The browser packaged version `chai.js` will ALWAYS contain all dependencies needed to run Chai.

## 1.6.1 / 2013-06-05

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required.
- **Plugin Developers:**
  - No changes required.
- **Core Contributors:**
  - Refresh `node_modules` folder for updated developement dependencies.

这个版本的变更对普通用户没有影响。

### Deep Equality

Regular Expressions are now tested as part of all deep equality assertions. In previous versions
they silently passed for all scenarios. Thanks to [@katsgeorgeek](https://github.com/katsgeorgeek) for the contribution.

现在正则表达式也可以进行深层相等的比较了。在以前的版中，此类比较在任何场景下都会静默地通过。

## 1.6.0 / 2013-04-29

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - No changes required.
- **Plugin Developers:**
  - No changes required.
- **Core Contributors:**
  - Refresh `node_modules` folder for updated developement dependencies.

这个版本的变更对普通用户没有影响。

### New Assertions
### 新的断言方法

#### Array Members Inclusion
#### “数组包含成员” 的断言

Asserts that the target is a superset of `set`, or that the target and `set` have the same members. Order is not taken into account. Thanks to [@NickHeiner](https://github.com/NickHeiner) for the contribution.

断定目标值是一个集合的超集，或断定目标值与一个集合拥有相同的成员。成员的排列顺序无关紧要。

```js
// (expect/should) full set
// (expect/should) 完整集合
expect([4, 2]).to.have.members([2, 4]);
expect([5, 2]).to.not.have.members([5, 2, 1]);

// (expect/should) inclusion
// (expect/should) 包含关系
expect([1, 2, 3]).to.include.members([3, 2]);
expect([1, 2, 3]).to.not.include.members([3, 2, 8]);

// (assert) full set
// (assert) 完整集合
assert.sameMembers([ 1, 2, 3 ], [ 2, 1, 3 ], 'same members');

// (assert) inclusion
// (assert) 包含关系
assert.includeMembers([ 1, 2, 3 ], [ 2, 1 ], 'include members');
```

#### Non-inclusion for Assert Interface
#### Assert 接口还有一个 “不包含” 断言方法

Most `assert` functions have a negative version, like `instanceOf()` has a corresponding `notInstaceOf()`.
However `include()` did not have a corresponding `notInclude()`. This has been added.

```js
assert.notInclude([ 1, 2, 3 ], 8);
assert.notInclude('foobar', 'baz');
```

## 1.5.0 / 2013-02-03

### Migration Requirements

The following changes are required if you are upgrading from the previous version:

- **Users:**
  - _Update [2013-02-04]:_ Some users may notice a small subset of deep equality assertions will no longer pass. This is the result of
  [#120](https://github.com/chaijs/chai/issues/120), an improvement to our deep equality algorithm. Users will need to revise their assertions
  to be more granular should this occur. Further information: [#139](https://github.com/chaijs/chai/issues/139).
- **Plugin Developers:**
  - No changes required.
- **Core Contributors:**
  - Refresh `node_modules` folder for updated development dependencies.

部分用户可能注意到，一小部分深层相等（deep equality）断言将不再通过了。原因在于 [#120](https://github.com/chaijs/chai/issues/120)，我们对深层相等的算法作了改进。如果遇到这种情况，用户需要把这些断言修改为更细粒度的方式。更多信息请参见 [#139](https://github.com/chaijs/chai/issues/139)。

### Usage Updates

#### For Users

**1. Component Support:** Chai now included the proper configuration to be installed as a
[component](https://github.com/component/component). Component users are encouraged to consult
[chaijs.com](http://chaijs.com) for the latest version number as using the master branch
does not gaurantee stability.

**1. 支持 Component**。

```js
// relevant component.json
  devDependencies: {
    "chaijs/chai": "1.5.0"
  }
```

Alternatively, bleeding-edge is available:

    $ component install chaijs/chai

**2. Configurable showDiff:** Some test runners (such as [mocha](http://visionmedia.github.com/mocha/))
include support for showing the diff of strings and objects when an equality error occurs. Chai has
already included support for this, however some users may not prefer this display behavior. To revert to
no diff display, the following configuration is available:

**2. 可配置的 showDiff 行为**。部分测试框架（比如 [mocha](http://visionmedia.github.com/mocha/)）支持在进行字符串（和对象）比较时显示差异对比（diff）信息。Chai 已经包含了对此功能的支持，不过如果有用户不需要这种行为，可以通过以下配置来禁用它：

```js
chai.Assertion.showDiff = false; // diff output disabled
                                 // diff 信息将禁用
chai.Assertion.showDiff = true; // default, diff output enabled
                                // 这是默认值，diff 信息将启用
```

（以下段落跟普通用户没关系，就不翻译了。）

#### For Plugin Developers

**1. New Utility - type**: The new utility `.type()` is available as a better implementation of `typeof`
that can be used cross-browser. It handles the inconsistencies of Array, `null`, and `undefined` detection.

- **@param** _{Mixed}_ object to detect type of
- **@return** _{String}_ object type

```js
chai.use(function (c, utils) {
  // some examples
  utils.type({}); // 'object'
  utils.type(null); // `null'
  utils.type(undefined); // `undefined`
  utils.type([]); // `array`
});
```

#### For Core Contributors

**1. Browser Testing**: Browser testing of the `./chai.js` file is now available in the command line
via PhantomJS. `make test` and Travis-CI will now also rebuild and test `./chai.js`. Consequently, all
pull requests will now be browser tested in this way.

_Note: Contributors opening pull requests should still NOT include the browser build._

**2. SauceLabs Testing**: Early SauceLab support has been enabled with the file `./support/mocha-cloud.js`.
Those interested in trying it out should create a free [Open Sauce](https://saucelabs.com/signup/plan) account
and include their credentials in `./test/auth/sauce.json`.
