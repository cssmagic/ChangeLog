---
title: "jQuery"
label: "change-log"
issue: "#5"
original: "https://blog.jquery.com/?s=jquery+released"
---

## 1.11.2- and 2.1.3-

（较早的版本先不翻译了）

## 1.11.3 and 2.1.4

_2015-04-28_ - [blog post](https://blog.jquery.com/2015/04/28/jquery-1-11-3-and-2-1-4-released-ios-fail-safe-edition/)

* These releases include a [hot-fix for a rare bug in iOS 8.2 and 8.3](https://github.com/jquery/jquery/issues/2145). This is the only change.
* [修复] ……

## 2.2.0

_2016-01-08_ - [blog post](https://blog.jquery.com/2016/01/08/jquery-2-2-and-1-12-released/)

（挺多，慢慢翻译……）

#### Ajax

* Remove workaround for IE6/7 ([e519098](https://github.com/jquery/jquery/commit/e5190982c40d7ac8ab9bdb2e7e4334f0e123ef66))
* remove event dependency from the ajax module ([4e7f34f](https://github.com/jquery/jquery/commit/4e7f34f6296111f7f91d621397dfb02c6bf4c41f))
* Fix for request aborted in ajaxSend ([#1775](https://github.com/jquery/jquery/issues/1775), [598ed05](https://github.com/jquery/jquery/commit/598ed050f6931922214aeaea8a1dc867e0cc6fb7))
* use anchor tag for parsing urls ([#1875](https://github.com/jquery/jquery/issues/1875), [b091fdb](https://github.com/jquery/jquery/commit/b091fdbafac33123cba329e6bb48b9281323ca38))
* simplify jQuery.parseXML method ([5a0867d](https://github.com/jquery/jquery/commit/5a0867d1e94794fbfc3be1f18f4c0a168dc18d95))
* Fix cross-domain detection test for non-default port ([83b038f](https://github.com/jquery/jquery/commit/83b038fc81ec12e29dba92ad022e1d5fcf4980bc))
* $.post and $.get can now take an options object ([#1986](https://github.com/jquery/jquery/issues/1986), [89ce0af](https://github.com/jquery/jquery/commit/89ce0af2cf7f001647e74fc1de92ce94a51fd5c2))
* simplify one ajax call and add explanatory comment ([0ac28ed](https://github.com/jquery/jquery/commit/0ac28ed293681cb8f2e9fdd11efa0021da039c84))
* make jQuery#load “type” field explicit ([4ef120d](https://github.com/jquery/jquery/commit/4ef120d3f2578fe3d52eb6c0d0641df945991391))
* replace “jqXHR.complete” callback with “always” ([97ef1f2](https://github.com/jquery/jquery/commit/97ef1f2612a9c5bd453d34146fdfd552cf9cee67))
* remove use of jQuery#each second argument ([a4715f4](https://github.com/jquery/jquery/commit/a4715f4216ace92fba6991106053415e66289686))
* remove “onunload” event handler ([a117dd0](https://github.com/jquery/jquery/commit/a117dd05f638a078c21dc57f19966f4ae81f98f0))
* Remove jsonp callbacks through “jQuery#removeProp” method ([#2323](https://github.com/jquery/jquery/issues/2323), [a2ae215](https://github.com/jquery/jquery/commit/a2ae215d999637e8d9d0906abcbf6b1ca35c8e6e))
* Account for Android 2.3 not firing window.onerror on script errors ([6044fb6](https://github.com/jquery/jquery/commit/6044fb6a7384aec85906949835ef9a58114896ce))
* do not quote “throws” option – use dot notation instead ([#2571](https://github.com/jquery/jquery/issues/2571), [c9cf250](https://github.com/jquery/jquery/commit/c9cf250daafe806818da1dd207a88a8e94a4ad16))
* correct indentation ([cb087ce](https://github.com/jquery/jquery/commit/cb087ce41daa5db4c8db10e586bdc141f953d93d))
* improve content-type detection ([#2584](https://github.com/jquery/jquery/issues/2584), [239169b](https://github.com/jquery/jquery/commit/239169bb2ede6ea6287d82d1d13b0c354f451749))
* trigger error callback on native abort ([#2079](https://github.com/jquery/jquery/issues/2079), [76e9a95](https://github.com/jquery/jquery/commit/76e9a95dbeaf28fbc5a64571ebb5959f91a9c14a))
* Don’t throw exceptions on binary data response ([#2498](https://github.com/jquery/jquery/issues/2498), [769446c](https://github.com/jquery/jquery/commit/769446c69775f6c44e35cee1bcdeccafba51be7b))
* code style fixes ([8a896df](https://github.com/jquery/jquery/commit/8a896dfac8ea9d7307d8819ab848fef9b03cd933))

#### Attr

* Use typeof check for getAttribute method ([075da30](https://github.com/jquery/jquery/commit/075da3091cda170bd8cd5ce47bad1c5b14760232))

#### Attributes

* exclusively lowercase A-Z in attribute names ([22c33bf](https://github.com/timmywil/jquery/commit/153acc1338073f1047b906fff8c9d1b9522c33bf))
* remove unnecessary element null check ([55ac56a](https://github.com/jquery/jquery/commit/55ac56aeda786a4d1b677aefd3f5bb134ecb02ad))
* Use the option val hook in select val hook and simplify it ([#1902](https://github.com/jquery/jquery/issues/1902), [f6302b0](https://github.com/jquery/jquery/commit/f6302b0b53d61dfe1adbfaf6612be5cbced5bbc1))
* fix failing test for new return value ([5dc4616](https://github.com/jquery/jquery/commit/5dc4616ca0fdbf2a80890bd9b236e796b84db8c1))
* add SVG class manipulation ([#2199](https://github.com/jquery/jquery/issues/2199), [20aaed3](https://github.com/jquery/jquery/commit/20aaed367f993f3c2aa204183d82d0d73efa114f))
* revert returning null for non-elements ([7632b74](https://github.com/jquery/jquery/commit/7632b7454b8a918b5eb9ade199a6a842eae98571))
* fix tabIndex on  in IE11 ([#2647](https://github.com/jquery/jquery/issues/2647), [c752a50](https://github.com/jquery/jquery/commit/c752a5030bc00eb5b45dea9c28963f824a5c4f44))
* revert returning null for non-existent attributes ([2905961](https://github.com/jquery/jquery/commit/2905961bf75b741937f430ee5b619f11e93a448d))
* removeClass() -> attr(“class”, “”) ([5db1e05](https://github.com/jquery/jquery/commit/5db1e053098af747330044d5740e5379f2834402))
* Use simpler boolean check vs a function call ([4bf1a09](https://github.com/jquery/jquery/commit/4bf1a09522955eb52de1fafb4ee1ecc5982b7a3e))
* return null when attribute does not exist ([#2118](https://github.com/jquery/jquery/issues/2118), [aaeed53](https://github.com/jquery/jquery/commit/aaeed53e9f1e299975cb6f697c8038ec3a83fa4d))

#### Authors

* Update AUTHORS.TXT and .mailmap ([03557db](https://github.com/jquery/jquery/commit/03557db96c5b9fad22320e94b52b118c89f7b6f9))

#### Build

* Update QUnit to latest (1.17.1) ([2d5c5d2](https://github.com/jquery/jquery/commit/2d5c5d213f09fa0205d07a2d60a36581058cc40a))
* Acknowledge Android 2.3 is not ES5-compatible ([#2478](https://github.com/jquery/jquery/issues/2478), [1c59b30](https://github.com/jquery/jquery/commit/1c59b308d201d6dd0f0aed2ad0256d01b9f68047))
* space between curly and paren is optional ([#2399](https://github.com/jquery/jquery/issues/2399), [63a577a](https://github.com/jquery/jquery/commit/63a577aa0bcb439c1730c3825407d86c128b17be))
* Moved JSHint directives to .jshintrc file ([15a609f](https://github.com/jquery/jquery/commit/15a609f7663c4348ab7f1acbc9e566ec20bb717c))
* update AUTHORS.txt ([8f13997](https://github.com/jquery/jquery/commit/8f13997e89ca325a49f7581fad7e85fe37bad166))
* Add a comment explaining why the es3 option is needed ([669cb16](https://github.com/jquery/jquery/commit/669cb16d763cb5486dadd56ec15a17b2b0303571))
* Upgrade to commitplease 2.0.0 ([5bc1ddc](https://github.com/jquery/jquery/commit/5bc1ddc5cc96e509e0fadb0c1e3a70927de6ed1c))
* Refactor Node smoke tests ([9c8a3ec](https://github.com/jquery/jquery/commit/9c8a3ecdc46156afd8f93aa44b6e6aea7c52c049))
* update version to 3.0.0-pre ([7a607c5](https://github.com/jquery/jquery/commit/7a607c5673fa36f9818f19e349871600a2938b1e))
* Fix various typos ([dc4b914](https://github.com/jquery/jquery/commit/dc4b914a05e1e6dbf13f916897b5d6a472ea0380))
* Update jscs and lint files ([#2056](https://github.com/jquery/jquery/issues/2056), [10fdad7](https://github.com/jquery/jquery/commit/10fdad742a2a6aa9f0e00b3e04fc5264797c53c7))
* correct jscs paths ([99975c4](https://github.com/jquery/jquery/commit/99975c44abc8c1092764c7fca3ccfe89fc832b87))
* Remove empty define({}) from build output ([#1768](https://github.com/jquery/jquery/issues/1768), [2c1b556](https://github.com/jquery/jquery/commit/2c1b556d98da597b0490f204e3561f656987f17c))
* correct style tests files which could be automatically corrected ([e35bdc1](https://github.com/jquery/jquery/commit/e35bdc1a22d7b5786b8f849acdc4653f1dc25e9b))
* Update commitplease dev dependency ([39b7606](https://github.com/jquery/jquery/commit/39b76064d9400295a383291ab6e821e259b67832))
* Update grunt-contrib-jshint ([1556c46](https://github.com/jquery/jquery/commit/1556c4661af647e355a9a5c0a814012955e231bc))
* remove bower.json lint target ([285cfbf](https://github.com/jquery/jquery/commit/285cfbfccc4c61d50ee8e0fe6e23695dc663e166))
* fix tests in AMD mode ([6051609](https://github.com/jquery/jquery/commit/6051609df35ef5e478c79c76534c03e4b46100bf))
* Update grunt-contrib-uglify because of a security issue in uglify ([835e921](https://github.com/jquery/jquery/commit/835e9218beef8f0c559da314fac01cb85dacb740))
* Update the license attribute ([#2331](https://github.com/jquery/jquery/issues/2331), [8e92e1e](https://github.com/jquery/jquery/commit/8e92e1ea3c533f3be82c99bbafaaf74b5bdedecc))
* update requirejs dependency to 2.1.17 ([#2290](https://github.com/jquery/jquery/issues/2290), [a644101](https://github.com/jquery/jquery/commit/a644101ed04d0beacea864ce805e0c4f86ba1cd1))
* bower.json: remove moot `version` field ([61e21a4](https://github.com/jquery/jquery/commit/61e21a4eaf479406b660328f4df7e3183c32386b))
* put back “lint” command to the “dev” list ([5adf04a](https://github.com/jquery/jquery/commit/5adf04a73c135dc729b9d9889bc963b45a9fc471))
* Upgrade to grunt-bowercopy 1.0.0 ([323e82c](https://github.com/jquery/jquery/commit/323e82c09f9078cc16f0df170e7a8bddea33523e))
* account for version labels in Sizzle versions ([#1939](https://github.com/jquery/jquery/issues/1939), [78ac753](https://github.com/jquery/jquery/commit/78ac753192d5490295a46b60f278c030d958bf6d))
* update node dependencies ([9101704](https://github.com/jquery/jquery/commit/91017047fc85cf634d9c7726901c250708f58731))
* Sizzle version labels must start with a dash ([d6c97ab](https://github.com/jquery/jquery/commit/d6c97abb744bfe8c67ab9158aecdb5bb1c05e47b))
* Don’t assume the browser environment; smoke test on Node w/ jsdom ([#1950](https://github.com/jquery/jquery/issues/1950), [76df9e4](https://github.com/jquery/jquery/commit/76df9e4e389d80bff410a9e5f08b848de1d21a2f))
* Remove dates from copyright notice ([66e1b6b](https://github.com/jquery/jquery/commit/66e1b6b8d49812239b5712d65922ff94c60f7b02))
* Specify valid components for commit messages ([0c9d018](https://github.com/jquery/jquery/commit/0c9d018889944da3d60cac135dc38dfcc37ac14a))
* Fix an email address of a contributor ([ab30934](https://github.com/jquery/jquery/commit/ab30934c1d7e023d9e80525c6e7ad4da31b543af))
* Remove unused Sizzle test files ([8d11310](https://github.com/jquery/jquery/commit/8d113104e980179e9eb4d092df0b1ab37cdc6fa5))
* Move all external libraries to external directory ([c5d9d88](https://github.com/jquery/jquery/commit/c5d9d88dce65b89a1d7d12b41ad254d5017a92a8))
* Don’t install jsdom 3 on Node.js 0.10 & 0.12 by default ([#2519](https://github.com/jquery/jquery/issues/2519), [dbb2daa](https://github.com/jquery/jquery/commit/dbb2daa8c3a458e3525d310440f4365548edc138))
* use different versions of jsdom for Node and iojs testing ([#2266](https://github.com/jquery/jquery/issues/2266), [5c3101f](https://github.com/jquery/jquery/commit/5c3101fee60046fa7976b3131fada8dfe9fbd53e))
* Rearrange grunt/npm tasks into a build/dist/test pattern ([bb928bd](https://github.com/jquery/jquery/commit/bb928bde7e7b85357fef3fedd450b04c03e965d7))
* Remove npm from dependencies ([b92acf7](https://github.com/jquery/jquery/commit/b92acf72372c3ad09d5f67ba3a1b2c19355a0e5f))
* Sanctify the component name status of Wrap ([a4133ff](https://github.com/jquery/jquery/commit/a4133ffafa6ac43b3aa22bc4edb4444b09f5250c))
* Drop io.js testing, test on latest Node.js ([250a199](https://github.com/jquery/jquery/commit/250a1990baa571de60325ab2c52eabb399c4cf9e))
* Use double quotes in .travis.yml ([06320c8](https://github.com/jquery/jquery/commit/06320c88af5be9cd937917282deb6eb4c4ad0443))
* Test on Node 5 ([cbe5b2b](https://github.com/jquery/jquery/commit/cbe5b2b79a46c61ad36ea5df44f80b1cc2c1b60a))
* Speed up the Travis build ([31f4f8e](https://github.com/jquery/jquery/commit/31f4f8e3f30e67e677a2aa167b9e894d46d5b81e))
* Remove a double empty line at the end of .travis.yml ([cea94a8](https://github.com/jquery/jquery/commit/cea94a83c7a5c5df6da578d417e5fb26152b19e1))
* ignore test dependencies for npm install ([35f8e15](https://github.com/jquery/jquery/commit/35f8e15fd73256ec02397d7bf93893e38afc9bc9))
* update Sizzle to 1.11.1 and include license ([c0b23e2](https://github.com/jquery/jquery/commit/c0b23e2b71eb7dd19b6435c6e94980275dd3990d))
* update grunt-bowercopy ([712e78c](https://github.com/jquery/jquery/commit/712e78c47fc3e550dabbb44055e5bf7877871bff))
* Add “deprecated” to the Testswarm module list ([1144e75](https://github.com/jquery/jquery/commit/1144e754a6a131bd4affec26fd85299e71bdab06))
* Update license ([4f776e5](https://github.com/jquery/jquery/commit/4f776e5ff91c48891f02d1ca3ba31132477d3972))
* update Sizzle ([#2042](https://github.com/jquery/jquery/issues/2042), [#1969](https://github.com/jquery/jquery/issues/1969), [3a0dd5a](https://github.com/jquery/jquery/commit/3a0dd5a3d3a23e81dfb32af2871fab6be4619434))
* Move test to appropriate module ([fbdbb6f](https://github.com/jquery/jquery/commit/fbdbb6fd431a3f598b581079b0ca37c399d369d4))
* update Sizzle to 2.0.0 ([bcca4f0](https://github.com/jquery/jquery/commit/bcca4f041b4c98dc9cb127ea3a2a7f40d2db4796))
* add mailmap entry ([3ec73ef](https://github.com/jquery/jquery/commit/3ec73efb26317239a4f22f0b023b0b99a4300a20))
* drop bower; use npm for front-end deps ([#15186](https://github.com/jquery/jquery/issues/15186), [e1949f4](https://github.com/jquery/jquery/commit/e1949f43711b5808d42378bafb6728b40b1738d6))
* update front-end dependencies ([8356948](https://github.com/jquery/jquery/commit/8356948ed4ee13af218af74c56c8a91ee9523828))
* fix broken assertions caused by QUnit update ([8b6aeae](https://github.com/jquery/jquery/commit/8b6aeae52d4c53a53468678ccd45e9dda9665004))
* Change the 2.2-stable version to 2.2.0-pre ([c56e8b6](https://github.com/jquery/jquery/commit/c56e8b680dbfcbcdff77d982618a8c6eda68cb49))
* Update native-promise-only (again) ([f5aa89a](https://github.com/jquery/jquery/commit/f5aa89af7029ae6b9203c2d3e551a8554a0b4b89))
* update Sizzle to 2.2.1 ([#2390](https://github.com/jquery/jquery/issues/2390), [44f8239](https://github.com/jquery/jquery/commit/44f8239d3f9d09d81e2885e9ae7e044277b67341))
* Update native-promise-only ([0065e1f](https://github.com/jquery/jquery/commit/0065e1f3e3021fc2bcb32e915177498bca034b34))
* remove deprecated JSHint options ([34da7d5](https://github.com/jquery/jquery/commit/34da7d552982d8ab7b18c2ceca9786d5023930f6))
* save sinon update for later ([#2160](https://github.com/jquery/jquery/issues/2160), [98c25b7](https://github.com/jquery/jquery/commit/98c25b7c803fe708a587f70e5b70541192004247))
* update node dependencies barring jscs ([8e3a0ce](https://github.com/jquery/jquery/commit/8e3a0ceafa2c7c78902d0eab07d21b793deb5366))
* update grunt-jscs-checker and pass with the new rules ([c869a1e](https://github.com/jquery/jquery/commit/c869a1ef8a031342e817a2c063179a787ff57239))
* update source map options for the new grunt jshint ([269a27c](https://github.com/jquery/jquery/commit/269a27c70204c7d233eac3cd91a383e9b5759a2f))
* Fixed issue with base path that contain ‘var’ ([#2450](https://github.com/jquery/jquery/issues/2450), [0c34e68](https://github.com/jquery/jquery/commit/0c34e688439713725d4215c63bc4cf876d8d0423))

#### Callbacks

* bring back size reduction ([f0532a2](https://github.com/jquery/jquery/commit/f0532a29e38d01d6f3e44435198527323d507cf9))
* No object starts out locked ([#1989](https://github.com/jquery/jquery/issues/1989), [0d829f0](https://github.com/jquery/jquery/commit/0d829f0e9a177038580a59d0b5649fab76b8104f))
* Disabling a callback should prevent firing ([#1790](https://github.com/jquery/jquery/issues/1790), [bc1cb12](https://github.com/jquery/jquery/commit/bc1cb122db30be034b3da84ee2546c86e2a5268f))
* Change broken url to wayback one ([31d58c5](https://github.com/jquery/jquery/commit/31d58c5cbbede6dc33d10feecd5277ccddb367e6))

#### CONTRIBUTING

* Condense info and add directions to other resources ([#1824](https://github.com/jquery/jquery/issues/1824), [bfd5dab](https://github.com/jquery/jquery/commit/bfd5dab2c6f387dce08e7c153ad0b3854ed971e4))
* Close parenthesis ([609adf6](https://github.com/jquery/jquery/commit/609adf63dadb7052c816b1a3ee44e3f928ede2e3))

#### Core

* Align branches: remove an unused variable, add comments ([f6de5a9](https://github.com/jquery/jquery/commit/f6de5a90ddde29e9096c2e45b9da21e65882b7c0))
* use interactive to evaluate dom ready, barring IE9-10 ([#2100](https://github.com/jquery/jquery/issues/2100), [dabd5ba](https://github.com/jquery/jquery/commit/dabd5ba96c05279b3ffb052db5b8d17f75996694))
* Test all factory use cases from intro.js ([#2181](https://github.com/jquery/jquery/issues/2181), [ab40725](https://github.com/jquery/jquery/commit/ab407258795bfa05756b009058757f8b42aa9c53))
* add workaround for iOS JIT error in isArrayLike ([#2145](https://github.com/jquery/jquery/issues/2145), [1541664](https://github.com/jquery/jquery/commit/154166458284bcce7d6a86328b7fd13483232a1a))
* CSS:Event: simplification of native method signatures ([85577a3](https://github.com/jquery/jquery/commit/85577a348a72ae765e0d7330b9e82985d23c94b7))
* allow init to accept an alternate rootjQuery for migrate’s sake ([#2101](https://github.com/jquery/jquery/issues/2101), [7a6931d](https://github.com/jquery/jquery/commit/7a6931de689865f559bed26e797e8cbb5674bbce))
* remove isArraylike check for nodes ([#2238](https://github.com/jquery/jquery/issues/2238), [436f0ae](https://github.com/jquery/jquery/commit/436f0aee0a4c37ecb61b87a3a44227f6f5153b3a))
* Standardize indexOf comparisons ([53aa87f](https://github.com/jquery/jquery/commit/53aa87f3bf4284763405f3eb8affff296e55ba4f))
* Support Symbol wrapper objects in jQuery.type ([8a73434](https://github.com/jquery/jquery/commit/8a734344f2566dab5b8d34ecd79ae81ebd8843c5))
* make isNumeric test work on Symbol ([0703fd5](https://github.com/jquery/jquery/commit/0703fd52ef88a2cdac93502070c51c93ffa1dfdd))
* CSS: disable 2 tests for Opera 12 ([13d2de7](https://github.com/jquery/jquery/commit/13d2de7efc1146bac018d2de49029e33b7b33af2))
* Remove unnecessary parameter to jQuery#constructor ([98cee73](https://github.com/jquery/jquery/commit/98cee73244d55910a1ac82bcf6cae04a7f650484))
* Update tested jsdom, drop obsolete workarounds ([#2153](https://github.com/jquery/jquery/issues/2153), [06f6cd1](https://github.com/jquery/jquery/commit/06f6cd1ffd2a4e9f5955d146d229492f245d83cb))
* change jQuery.each and jQuery#each signatures ([#2090](https://github.com/jquery/jquery/issues/2090), [2380028](https://github.com/jquery/jquery/commit/2380028ec4a6a77401b867a51de26a3cb8e8d311))
* re-introduce createHTMLDocument in parseHTML; Safari 8 left out ([cfe468f](https://github.com/jquery/jquery/commit/cfe468f29c4cbe1a457d0feb17dec90dcfd7c280))
* revert addition of createHTMLDocument. Thanks, Safari 8\. ([b779831](https://github.com/jquery/jquery/commit/b77983173e18724a883e02ad3a84661e18e6cf4a))
* Consistently use local reference to access() ([2fb719e](https://github.com/jquery/jquery/commit/2fb719e5aa885232c5347576e9f9e1e341a7ba15))
* pass empty string to createHTMLDocument to appease IE ([31c7d7f](https://github.com/jquery/jquery/commit/31c7d7fb7530e1af950b41d13dd956820d5c6908))
* remove unnecessary support test for createHTMLDocument ([5923282](https://github.com/jquery/jquery/commit/59232825aa87b941dd2418a6860b64017dfec0ae))
* use document.implemenation.createHTMLDocument in jQuery.parseHTML ([58c2460](https://github.com/jquery/jquery/commit/58c24608210c9a9a264a38746628ebc26823f59b))
* Simplify and speed up .each ([eeda11c](https://github.com/jquery/jquery/commit/eeda11cdd6a69ec2ef4e9c1ed12b82a79910fda5))
* simplify “each” stylesheet iteration test ([fcb6c4d](https://github.com/jquery/jquery/commit/fcb6c4d1d6552c7e54df16a36b171858bdf0553f))
* add unit test for isPlainObject(Symbol) ([#2645](https://github.com/jquery/jquery/issues/2645), [9090d98](https://github.com/jquery/jquery/commit/9090d98439f8dc449beafee98f8ff35cfb4f9116))
* Follow the AMD specification for define ([892625b](https://github.com/jquery/jquery/commit/892625b3c36eda6bb6ac226d15e0a158ba35cf21))
* Make jQuery objects iterable ([#1693](https://github.com/jquery/jquery/issues/1693), [bb026fc](https://github.com/jquery/jquery/commit/bb026fc12c3c2ad37f47f0919e484bddcdc3d291))
* Use window.setTimeout & friends instead of global equivalents ([#2177](https://github.com/jquery/jquery/issues/2177), [219c749](https://github.com/jquery/jquery/commit/219c7494938a10b985b7827990bc419e41585b10))
* Don’t expose jQuery.access ([#2513](https://github.com/jquery/jquery/issues/2513), [9adfad1](https://github.com/jquery/jquery/commit/9adfad19865837f5dffedb1eb41e407f196ca515))
* Switch from modules to just window.setTimeout etc. ([842958e](https://github.com/jquery/jquery/commit/842958e7aecd0d75a7ee9e2aaec83457701aa2f3))
* Drop strundefined variable ([29838b6](https://github.com/jquery/jquery/commit/29838b6cab6f2e508f3e9692f32918c72b1a504b))
* organize prop & attr code to be similar ([5153b53](https://github.com/jquery/jquery/commit/5153b5334eb2c8317372b46209bd9d092a91afdc))
* Adjust comments & tests after dropping Safari 6 support ([93bee47](https://github.com/jquery/jquery/commit/93bee4701d14202045a88aab156da0daf9418430))
* .each/.map should accept an undefined/null value ([#2267](https://github.com/jquery/jquery/issues/2267), [bf48c21](https://github.com/jquery/jquery/commit/bf48c21d225c31f0f9b5441d95f73615ca3dcfdb))
* Add a support comment for Safari 8 ([d242753](https://github.com/jquery/jquery/commit/d24275372624bac897c4131fd1507a58c09a1483))

#### Css

* Fix the “sanity check” test ([995f707](https://github.com/jquery/jquery/commit/995f70777ac6c0f988a44807ef1399e73937b2ee))
* Remove non-functional unit test for negative margin ([4ab7431](https://github.com/jquery/jquery/commit/4ab743188ec6bdaafe8550dab84f374ef7e22aca))

#### CSS

* fix :visible/:hidden selectors for inline element w/ content ([#2227](https://github.com/jquery/jquery/issues/2227), [79bcb29](https://github.com/jquery/jquery/commit/79bcb291324167ab2d844027d0cdc6300613d010))
* save 20 bytes in css/support ([45ec73f](https://github.com/jquery/jquery/commit/45ec73f55618cd080867a98b42b9ab80409cab2e))
* Don’t name the anonymous swap function ([0019a46](https://github.com/jquery/jquery/commit/0019a463bdcb81dc6ba3434505a45774ca27f363))
* Correct misrepresentation of “auto” horizontal margins as 0 ([#2237](https://github.com/jquery/jquery/issues/2237), [487d5ca](https://github.com/jquery/jquery/commit/487d5ca913c237aafe9efa1179749b46382fddbf))
* Use pre-defined displays for html and body ([a772418](https://github.com/jquery/jquery/commit/a7724186c98734529b06bebb8f2dc7fc2b641011))
* Support relative adjustment in any applicable unit ([#1711](https://github.com/jquery/jquery/issues/1711), [9b03f6d](https://github.com/jquery/jquery/commit/9b03f6df88a8d9dbda3f7893cdd84e3a3c70da17))
* use isFinite in place of redundant isNumeric ([3689963](https://github.com/jquery/jquery/commit/3689963909880ed832ac17eabf7b9260927a68d8))
* Clean up memory leak in reliableMarginRight ([#1795](https://github.com/jquery/jquery/issues/1795), [7d15b4d](https://github.com/jquery/jquery/commit/7d15b4d1f181de8868c375c545a51e4dfc28a611))
* Correct typo in the comment ([7e09619](https://github.com/jquery/jquery/commit/7e09619cdf2813f2cd9da600ba682be8f91b08b6))
* elements are hidden when either offsetWidth or offsetHeight is zero ([#10406](https://github.com/jquery/jquery/issues/10406), [#13132](https://github.com/jquery/jquery/issues/13132), [10399dd](https://github.com/jquery/jquery/commit/10399ddcf8a239acc27bdec9231b996b178224d3))
* Add animation-iteration-count to cssNumber, fix tests ([#2792](https://github.com/jquery/jquery/issues/2792), [b9a6958](https://github.com/jquery/jquery/commit/b9a695865b4eb3916f7320026d028a2866da6e4e))
* Don’t cache unrecognized CSS property names ([#2015](https://github.com/jquery/jquery/issues/2015), [d471842](https://github.com/jquery/jquery/commit/d471842b3e3af83c9a1be06b5d16f75bfa96af8c))
* Collapse a double if statement into one ([7855a1a](https://github.com/jquery/jquery/commit/7855a1a7d8a5c959d4ef2f951b4eb971908ac96f))
* Add unit tests for negative margins and positioning ([1b932bb](https://github.com/jquery/jquery/commit/1b932bb7867924b98529537f8ccd35db979ae22a))
* Work around an IE11 fullscreen dimensions bug ([#1764](https://github.com/jquery/jquery/issues/1764), [90d828b](https://github.com/jquery/jquery/commit/90d828bad0d6d318d73d6cf6209d9dc7ac13878c))
* Restore the hack to get pixels for .css(‘width’) etc. ([3747cc6](https://github.com/jquery/jquery/commit/3747cc642a48d2a5a8ac83069f66bddd33bea301))
* make the getStyles function more readable ([3a0d582](https://github.com/jquery/jquery/commit/3a0d582cf63b6e8f77150d9c38d2bf34d0c7790e))
* Fix the pixelMarginRight support test in Android 2.3 ([cdfc2d0](https://github.com/jquery/jquery/commit/cdfc2d092afad5a3e5b3978b04b402a1ee9dce79))
* Don’t expose jQuery.swap ([#2058](https://github.com/jquery/jquery/issues/2058), [bb4d888](https://github.com/jquery/jquery/commit/bb4d888f4f7886371347b59eae5d4e6135acb7ed))
* simplify “defaultDisplay” module ([c62486f](https://github.com/jquery/jquery/commit/c62486fb4cb18fdb7dc5807231c964ed82ee6482))
* Improve a comment explaining IE11 fullscreen bug ([8e4aac8](https://github.com/jquery/jquery/commit/8e4aac8cb03ffb88373ea99629165d82ff5eccdd))
* Add an integration test for issue gh-1764 ([8887106](https://github.com/jquery/jquery/commit/8887106702baa69ed80baa65c5a249786bffc77e))
* Removed redundant “to the number” in comment ([895ea68](https://github.com/jquery/jquery/commit/895ea6887dd02a44067d041db00c355c80e930a3))
* Remove use of getDefaultComputedStyle ([#15227](https://github.com/jquery/jquery/issues/15227), [274feb5](https://github.com/jquery/jquery/commit/274feb53cc9a99633dfac785d8b3b837d192c43c))

#### Data

* move element cache to element[expando] ([#1734](https://github.com/jquery/jquery/issues/1734), [d702b76](https://github.com/jquery/jquery/commit/d702b7637a61e1973e08c27b8d8de2ed24a543e2))
* updates to element[expando] cache ([222ac3a](https://github.com/jquery/jquery/commit/222ac3ad6bd40ef4dfb4e4c60bac4b751d907e2a))
* shave off a couple of bytes ([6f65f5f](https://github.com/jquery/jquery/commit/6f65f5faf2b5831414d4c93d271a59265b41a75b))
* restore explicit data removal of private data in cleanData. ([#2127](https://github.com/jquery/jquery/issues/2127), [332fd94](https://github.com/jquery/jquery/commit/332fd941b4ae80e8ca5e5a20aca91806038f4816))
* remove user data in cleanData ([#2503](https://github.com/jquery/jquery/issues/2503), [5fe76c6](https://github.com/jquery/jquery/commit/5fe76c663f8a4986af62edb434a1708c006d0b21))
* avoid Object.defineProperties for nodes ([#1728](https://github.com/jquery/jquery/issues/1728), [95fb798](https://github.com/jquery/jquery/commit/95fb798980d7e404c413e29e20016db9052e2bf2))
* speed up $.fn.data() for camel-cased key ([#1941](https://github.com/jquery/jquery/issues/1941), [72c4a06](https://github.com/jquery/jquery/commit/72c4a067a9def9720a997f23615690970894dc9c))
* find hyphenated data with camelCased key ([#2779](https://github.com/jquery/jquery/issues/2779), [c1511c6](https://github.com/jquery/jquery/commit/c1511c673148208ab17cafa0faf37bce3b4ae392))
* avoid non-alphanumeric chars in expando properties ([0cdec79](https://github.com/jquery/jquery/commit/0cdec797de23555c95a70978f4d9e06f3b041330))
* Drop the tests relying on applets ([#1938](https://github.com/jquery/jquery/issues/1938), [95c0a10](https://github.com/jquery/jquery/commit/95c0a10e15477a5031185e2d656d896905562afa))
* Combine register and cache methods ([b5f7c9e](https://github.com/jquery/jquery/commit/b5f7c9e2d526b17b9962976bb704dce8779d7362))
* avoid using delete on DOM nodes ([0e98243](https://github.com/jquery/jquery/commit/0e982433eb94391b3e9f6838d9b8fbf9bb31abf9))
* Don’t expose jQuery.acceptData ([#2555](https://github.com/jquery/jquery/issues/2555), [2242719](https://github.com/jquery/jquery/commit/224271982eb9cd351d7db1b38c740b4e927e6f97))
* Use a PDF object instead of a Java applet for acceptData testing ([#1938](https://github.com/jquery/jquery/issues/1938), [087d280](https://github.com/jquery/jquery/commit/087d280ad1160de53a45ea96184911194f7b46e0))
* do not create data cache when fetching single property ([f5bf9bc](https://github.com/jquery/jquery/commit/f5bf9bc48897e3b8f050d87d02252c8be456044a))
* remove the expando when there’s no more data ([#1760](https://github.com/jquery/jquery/issues/1760), [56bb677](https://github.com/jquery/jquery/commit/56bb677725b21415905e5c3eeb1e05be4480e780))
* remove some unused code ([764dc94](https://github.com/jquery/jquery/commit/764dc949d0d65742606747ce75852d1b5dd59fcd))

#### Deferred

* Fix $.when with resolved deferred and progress callbacks ([#1894](https://github.com/jquery/jquery/issues/1894), [ab20d9d](https://github.com/jquery/jquery/commit/ab20d9d24f0a95df382c02e9ef3dcc4adb86e4f1))
* Always handle progress callbacks before done/fail ([#2013](https://github.com/jquery/jquery/issues/2013), [#2010](https://github.com/jquery/jquery/issues/2010), [002240a](https://github.com/jquery/jquery/commit/002240a6eb1cee2fcd886d5cf44893eb67f246f1))

#### Deprecated

* fix amd mode for the deprecated module ([e271f66](https://github.com/jquery/jquery/commit/e271f665dd8fb617a5015051e1c9df8cebd6c97b))

#### Dimensions

* properly manipulate non-px values ([#1712](https://github.com/jquery/jquery/issues/1712), [75b3cdd](https://github.com/jquery/jquery/commit/75b3cdd509a2cf0a704767d04557ec392112a438))
* allow modification of coordinates argument ([#1848](https://github.com/jquery/jquery/issues/1848), [f7e60dc](https://github.com/jquery/jquery/commit/f7e60dc83d81cbf892de9dab39642dd67c49bd23))

#### Docs

* Fix README uppercase ([b50e0f2](https://github.com/jquery/jquery/commit/b50e0f2c3651d64d40931a16733b015f56409c63))
* remove redundant instruction from the readme ([#2359](https://github.com/jquery/jquery/issues/2359), [3c92770](https://github.com/jquery/jquery/commit/3c9277086742fe3a38a268ef97184be34e294655))
* correct grunt command in README.md ([#1850](https://github.com/jquery/jquery/issues/1850), [9d6beac](https://github.com/jquery/jquery/commit/9d6beac3958da79671344fd11b9a3fe9b85f88e1))
* 1.x-master branch -> compat branch; 2.x branch -> master branch ([758fd6c](https://github.com/jquery/jquery/commit/758fd6cea9e82f7bfebce07ba6ecf0d107e8a53c))
* Clarify custom build instructions ([a3779bc](https://github.com/jquery/jquery/commit/a3779bc3254159f5a99e8204e69a0f0b9e191f6f))
* Add info about Sizzle not being excludable on the compat branch ([#2184](https://github.com/jquery/jquery/issues/2184), [062b526](https://github.com/jquery/jquery/commit/062b5267d0a3538f1f6dee3df16da536b73061ea))
* Fix various spelling mistakes ([360a478](https://github.com/jquery/jquery/commit/360a4780339b7f412b75ad8a06dca7f39616f654))
* “npm run build” was missing from the contributing guides ([735dea3](https://github.com/jquery/jquery/commit/735dea34fb0ae625542d51eae3f4e7316e403eaa))

#### Effects

* set default easing using jQuery.easing._default ([#2219](https://github.com/jquery/jquery/issues/2219), [5f2ea40](https://github.com/jquery/jquery/commit/5f2ea402582c7b8f4773771e1529d60587f3435e))
* Remove tests for jQuery.Animation & jQuery.Tween ([a5864ae](https://github.com/jquery/jquery/commit/a5864aefdfadfee16522456c82139fa10360d8fc))
* Improve raf logic ([708764f](https://github.com/jquery/jquery/commit/708764f47b0c8de152bbb444d0f608db558b76ed))
* Finish should call progress ([#2283](https://github.com/jquery/jquery/issues/2283), [3dd3d13](https://github.com/jquery/jquery/commit/3dd3d1357d027a487559516fcdd9064cc792edab))
* manually revert two `requestAnimationFrame` commits ([0a98623](https://github.com/jquery/jquery/commit/0a98623abb85bdce079b400ed3bf3d87ddc6b1da))
* add tests for jQuery.easing._default in Animation and Tween ([6d7ef56](https://github.com/jquery/jquery/commit/6d7ef56ed3004a18f5139928455cdbdc169e1232))
* Add tests for jQuery.Tween ([cdaed15](https://github.com/jquery/jquery/commit/cdaed15c7ea1bbfdde5a5bea691c583ce7961526))
* Adding unit tests for jQuery.Animation ([b3b2d6c](https://github.com/jquery/jquery/commit/b3b2d6c3dd51fbdc69e1942e9af75cc99a1834c2))
* Reintroduce use of requestAnimationFrame ([#15147](https://github.com/jquery/jquery/issues/15147), [72119e0](https://github.com/jquery/jquery/commit/72119e0023dcc0d9807caf6d988598b74abdc937))

#### Event

* HTML5 drop events inherit from MouseEvent ([#2009](https://github.com/jquery/jquery/issues/2009), [d7e5fce](https://github.com/jquery/jquery/commit/d7e5fcee519e5f3e840beef9e67a536e75133df9))
* Ensure delegation doesn’t error on comment nodes ([#2055](https://github.com/jquery/jquery/issues/2055), [493b0fd](https://github.com/jquery/jquery/commit/493b0fd7f51054345abe981270bd7839825f79dd))
* remove preDispatch hook & simplify “simulate” signature ([3655c4e](https://github.com/jquery/jquery/commit/3655c4e1908cc3ee49487e7e26e8cfca9fe8146d))
* Copy detail property to jQuery.Event on native events ([#1867](https://github.com/jquery/jquery/issues/1867), [d9ed166](https://github.com/jquery/jquery/commit/d9ed166c865e91ccc8cef1ca282785c500ca2306))
* Fully clean up events in unit test ([4467ed6](https://github.com/jquery/jquery/commit/4467ed606ab0a9b28ed495e682576910937fa5e0))
* Update support comments for mouseenter/mouseleave implementation ([2792845](https://github.com/jquery/jquery/commit/2792845534e36c39dbb9c8369ed96aaefa560081))
* Add a note about a mouseenter bug in Chrome ([a5e1c9b](https://github.com/jquery/jquery/commit/a5e1c9b44c971fd7046d9a95bd0810e50840b663))
* Empty namespaces should be uneventfully ignored ([8653068](https://github.com/jquery/jquery/commit/8653068dd6b8a515f5c1d8a0fda4479e9534103e))
* remove outdated originalEvent hack ([6df669f](https://github.com/jquery/jquery/commit/6df669f0fb87cd9975a18bf6bbe3c3548afa4fee))
* Remove fake originalEvent from jQuery.Event.simulate ([#2300](https://github.com/jquery/jquery/issues/2300), [7475d5d](https://github.com/jquery/jquery/commit/7475d5debeb7c53158921ed40f6c2fdb25a2cc86))
* Add basic unit tests for event aliases ([#2302](https://github.com/jquery/jquery/issues/2302), [e05c63e](https://github.com/jquery/jquery/commit/e05c63e17a037d550e7dde5d805ee5c4214ee44b))
* Fix delegated radio events when arrow keys are used ([#2343](https://github.com/jquery/jquery/issues/2343), [c82a668](https://github.com/jquery/jquery/commit/c82a6685bb964627e27008e298f93ea81218265b))
* Make event aliases optional in unit tests ([2cb8eba](https://github.com/jquery/jquery/commit/2cb8ebadcb77da1c1a12c07bc5274fd456bf3b01))
* provide verbose comment for focus(in | out) & rename support prop ([c074006](https://github.com/jquery/jquery/commit/c074006a69db73a116dc04ec78844468a8cea7d3))
* Move .bind() and .delegate() to deprecated ([#2288](https://github.com/jquery/jquery/issues/2288), [ee0854f](https://github.com/jquery/jquery/commit/ee0854f85bd686b55757e8854a10480f23c928da))
* Separate trigger/simulate into its own module ([#1864](https://github.com/jquery/jquery/issues/1864), [c9935b6](https://github.com/jquery/jquery/commit/c9935b6d2db9e1be4bed12f7419e98cdca45763e))
* Move VML test out of event alias test ([67fa2ea](https://github.com/jquery/jquery/commit/67fa2eab6ef323b1d894e9e7f054c6e8c844d304))
* Remove an internal argument to the on method ([04a2969](https://github.com/jquery/jquery/commit/04a29696e5b176ac66401120e433d52425222f0f))
* fix incorrect window bug with scrollTop/Left in iframes ([#1945](https://github.com/jquery/jquery/issues/1945), [d21edb5](https://github.com/jquery/jquery/commit/d21edb599d8f5f80a3f3ecba5b62311b9cd1a3e6))
* fix incorrect test ([d923100](https://github.com/jquery/jquery/commit/d92310050ca7bf0b33825d64e052f9a8809c3e9e))
* Restore the `constructor` property on jQuery.Event prototype ([#15090](https://github.com/jquery/jquery/issues/15090), [b807aed](https://github.com/jquery/jquery/commit/b807aedb7fee321fb3aa5d156a5a256ab0634e2d))
* Only check elements for delegation matches ([9d820fb](https://github.com/jquery/jquery/commit/9d820fbde6d89bc7a06e2704be61cf6c0b4d6e3c))
* remove redundant guards for the event methods ([#2047](https://github.com/jquery/jquery/issues/2047), [a873558](https://github.com/jquery/jquery/commit/a873558436383beea7a05fd07db7070a30420100))
* add support comment ([9db9316](https://github.com/jquery/jquery/commit/9db9316609c2881dbb6abc49efc3aa91a57a02ad))
* correct support comment ([361a0d5](https://github.com/jquery/jquery/commit/361a0d5150a1c57b1857611cde1b05bd0ef21a50))
* Normalize mouse event properties in drag events ([#1925](https://github.com/jquery/jquery/issues/1925), [97cf528](https://github.com/jquery/jquery/commit/97cf5280824027c3d4fcdbb4db49c10ad3c62bce))

#### Manipulation

* Make an HTML interception point ([#1747](https://github.com/jquery/jquery/issues/1747), [225bde3](https://github.com/jquery/jquery/commit/225bde37c997f5ddd9fe00fdfb8e9a43545cfbbc))
* add support to tag-hyphenated elements ([#1987](https://github.com/jquery/jquery/issues/1987), [85ffc6d](https://github.com/jquery/jquery/commit/85ffc6d973865a031ded170934e0acfc2e97cb11))
* Detect sneaky no-content replaceWith input ([#2204](https://github.com/jquery/jquery/issues/2204), [4b27ae1](https://github.com/jquery/jquery/commit/4b27ae16a2b911f75b341b56d9d939bc65a9657a))
* Tolerate XMLNode host object input to getAll ([#15151](https://github.com/jquery/jquery/issues/15151), [1ae025e](https://github.com/jquery/jquery/commit/1ae025e24f9920d18cec8a8498bfc4eed7e3f1dc))
* Check state lost if the name is set for Android 4.0-4.3 ([1bbb678](https://github.com/jquery/jquery/commit/1bbb678949da480dce0d9ed3d0fb273bccce9787))
* privatize internal domManip() function ([#2225](https://github.com/jquery/jquery/issues/2225), [62d5579](https://github.com/jquery/jquery/commit/62d5579578109f1468a37e44f76af06f283a46ab))
* privatize buildFragment() function ([#2224](https://github.com/jquery/jquery/issues/2224), [a74320f](https://github.com/jquery/jquery/commit/a74320fca8bb0a2190f6e1fdb71a73733b6986e4))
* Remove an internal argument to the remove method ([#2301](https://github.com/jquery/jquery/issues/2301), [349edbd](https://github.com/jquery/jquery/commit/349edbd6c53aa93d4fd207d3c0c4c24a7b0314dd))
* Don’t provide the parser with sloppy table markup ([#2493](https://github.com/jquery/jquery/issues/2493), [99e8ff1](https://github.com/jquery/jquery/commit/99e8ff1baa7ae341e94bb89c3e84570c7c3ad9ea))
* re-expose domManip until 3.0 ([#2225](https://github.com/jquery/jquery/issues/2225), [6ed6bc3](https://github.com/jquery/jquery/commit/6ed6bc335f98352acfc7c07249bc4e936099aecf))
* simplify html wrappers ([#2002](https://github.com/jquery/jquery/issues/2002), [0ea342a](https://github.com/jquery/jquery/commit/0ea342a6a6dce793c1b0f14f051c2573f40f4e44))
* Switch rnoInnerhtml to a version more performant in IE ([#2563](https://github.com/jquery/jquery/issues/2563), [d4def22](https://github.com/jquery/jquery/commit/d4def22e4cd1c2eb2571f449e226b38384fb6d81))
* don’t auto-insert tbody ([#1835](https://github.com/jquery/jquery/issues/1835), [e984d1c](https://github.com/jquery/jquery/commit/e984d1c79cc476062818e03df04a366baa13d197))
* add support to tag-hyphenated elements ([83f24e5](https://github.com/jquery/jquery/commit/69dda5b56b8199f9f9df3f1761538ba0183f24e5))

#### Misc

* Mac OS is now OS X, thanks @xfq ([d30c482](https://github.com/jquery/jquery/commit/d30c482910bf35c5dbaec9c82174d1e6ae8839b5))
* Fix the tests, revert some unneeded/broken reverts ([1ad9915](https://github.com/jquery/jquery/commit/1ad9915d11e27ebce8016ef81163206fb68b2335))
* Need for speed removed by 9ad6e7e ([ff928f5](https://github.com/jquery/jquery/commit/ff928f5775566ee54f26fcb0f9a326719c32e63c))
* Update all references to bugs.jquery.com ([#1681](https://github.com/jquery/jquery/issues/1681), [3e89a53](https://github.com/jquery/jquery/commit/3e89a53265bfdc992d7a97a01c5d1025e48e5906))
* Remove leftover -moz-box-sizing in tests ([e81b258](https://github.com/jquery/jquery/commit/e81b258ace257ba138022cf28374190623b0be5e))
* Adjust comments & docs to dropping IE<8 in jQuery Compat ([c309b95](https://github.com/jquery/jquery/commit/c309b95756b83b60fadc369edb120db4520c364a))

#### Offset

* offsetLeft/Top on empty set returns undefined ([#2319](https://github.com/jquery/jquery/issues/2319), [2937019](https://github.com/jquery/jquery/commit/29370190605ed5ddf5d0371c6ad886a4a4b5e0f9))
* allow offset setter to throw for disconnected elements ([#2114](https://github.com/jquery/jquery/issues/2114), [0d11c11](https://github.com/jquery/jquery/commit/0d11c1182f2012cd6eb06ce1e3fa5a495af9bee3))
* allow small differences in offset.top ([#2590](https://github.com/jquery/jquery/issues/2590), [9f9e204](https://github.com/jquery/jquery/commit/9f9e204bba41b7a9cde5ba7e065d817ef8b18c41))
* don’t run scrollTop/scrollLeft iframe test in Android 2.3 & 4.0 ([#1981](https://github.com/jquery/jquery/issues/1981), [0c46643](https://github.com/jquery/jquery/commit/0c466438d1feaec302fec13eafeeb063bbfd6a19))
* add tests for hidden elements + scroll ([b041242](https://github.com/jquery/jquery/commit/b04124222395a05c80d4f1c3a70333fdb07bfe3d))
* return before getBoundingClientRect to avoid error in IE8-11 ([0e4477c](https://github.com/jquery/jquery/commit/0e4477c676db0427bb9b0bf39df8631501e62f24))
* Round offset value for the sake of floating errors ([#2147](https://github.com/jquery/jquery/issues/2147), [62ae2d0](https://github.com/jquery/jquery/commit/62ae2d0fb7ac011bf2ad778f8158de408e785927))
* return zeros for disconnected/hidden elements ([#2310](https://github.com/jquery/jquery/issues/2310), [40dcc76](https://github.com/jquery/jquery/commit/40dcc767640c41a4387a343f1ef53ac57ed631c5))
* Simplified a conditional ([4287442](https://github.com/jquery/jquery/commit/4287442ab8bdf8d9f008f3e84ccbf7d86d0fb5db))
* account for scroll when calculating position ([#1708](https://github.com/jquery/jquery/issues/1708), [2d71594](https://github.com/jquery/jquery/commit/2d715940b9b6fdeed005cd006c8bf63951cf7fb2))
* don’t run scrollTop/scrollLeft iframe test in mobile Safari ([4ab8603](https://github.com/jquery/jquery/commit/4ab8603669e2bbc8644e402927c33ce422d7aaa3))
* simplify jQuery#offsetParent method ([74ae544](https://github.com/jquery/jquery/commit/74ae5444832b2fb966768a97281d2ad8c088bc58))
* do not run tests which break without back-incompat change ([9d1d4c2](https://github.com/jquery/jquery/commit/9d1d4c272a58ced36242d90b3f0462c2bbb972a3))

#### Readme

* Fix minor style issues. Thanks @MightyBranch! ([edfc94d](https://github.com/jquery/jquery/commit/edfc94df92982c2d840f6692291e09211d1c7cfc))
* Fix punctuation in tile ([df62159](https://github.com/jquery/jquery/commit/df62159296e9de8b04653ba999a32f9be7bb2a73))

#### README

* Improve build instructions ([2e9c1ea](https://github.com/jquery/jquery/commit/2e9c1ead76aaae8fde004e3cacde1e36c5fd2104))
* Update the description of the deprecated module ([1d75273](https://github.com/jquery/jquery/commit/1d752731011d35e985271334ff98186728949f03))
* various text fixes ([31b63fc](https://github.com/jquery/jquery/commit/31b63fc23674ede657f019783ad7b942bb83f9c3))
* Add selector-native.js link. Thanks @randsonjs! ([cfe2eae](https://github.com/jquery/jquery/commit/cfe2eae38df411c0f15cbbf927612bc515063bf5))
* update the Homebrew site address ([b410b15](https://github.com/jquery/jquery/commit/b410b15e8da1a8d285f431640ff165e634196115))

#### Release

* bower.json is actually generated from scratch ([61224f5](https://github.com/jquery/jquery/commit/61224f5fef4336cd47cb26be74f9758096f7f956))
* update AUTHORS.txt ([ae3229c](https://github.com/jquery/jquery/commit/ae3229c805705a01603b8f1fb094528f43b05168))
* Distribute files to distribution repo ([#1869](https://github.com/jquery/jquery/issues/1869), [#1673](https://github.com/jquery/jquery/issues/1673), [#2045](https://github.com/jquery/jquery/issues/2045), [26eca14](https://github.com/jquery/jquery/commit/26eca143c2dd857b9e3d1c446a467fed16e903d2))
* remove antiquated release-notes.js ([7bb39f3](https://github.com/jquery/jquery/commit/7bb39f35118c33f1f7effc49112579ec9393f02c))
* properly set the dist remote when it’s a real release ([c44dd77](https://github.com/jquery/jquery/commit/c44dd7775b387094d8c921c7e839e3c266e4f2c8))
* remove revert artefacts ([3655260](https://github.com/jquery/jquery/commit/3655260866cdcfe42a1117bfb9603144c9e4d829))
* update AUTHORS.txt ([e905dcd](https://github.com/jquery/jquery/commit/e905dcd8f33e99275e29b0333e7b255559197c81))
* fix revert artefacts ([e2af987](https://github.com/jquery/jquery/commit/e2af987877c83e5b054e1f9cac1a8534ebed0b18))
* allow local and github dists ([47c21ef](https://github.com/jquery/jquery/commit/47c21efce522204d0c3e779faa10de2ee63cedd7))
* ensure files are copied to dist ([b4e139c](https://github.com/jquery/jquery/commit/b4e139cb7bdd890c0bf7d1c64f112e44100598a5))
* Remove copying of jquery-latest files ([c34ed46](https://github.com/jquery/jquery/commit/c34ed46eee12c92cb050a53eb62daf9e1258caf9))
* remove revert artefacts ([c69673f](https://github.com/jquery/jquery/commit/c69673fe41ee17f46545e87a31ff96cea6c68a17))
* push dist to same remote as project ([1ba45fc](https://github.com/jquery/jquery/commit/1ba45fcc15c894cad591d93cbb88010df5f235fe))
* fix revert artefacts ([ae88b39](https://github.com/jquery/jquery/commit/ae88b3971c38e0d32a8b927d597426bb50263c6f))
* remove sourcemap comment from all copies of minified file ([#1707](https://github.com/jquery/jquery/issues/1707), [a76c781](https://github.com/jquery/jquery/commit/a76c7812366e7e45ea29969db72d90261ef87af5))
* fix CDN archive creation ([#1940](https://github.com/jquery/jquery/issues/1940), [e0673df](https://github.com/jquery/jquery/commit/e0673dfedb9ad07d8e68f28a54453b975c412c33))
* dist can be run during a test ([aae998b](https://github.com/jquery/jquery/commit/aae998b5449f35dc71e87e360aee5bd0022e7c8e))

#### Selector

* pass jQuery unit tests with selector-native ([#1742](https://github.com/jquery/jquery/issues/1742), [#2048](https://github.com/jquery/jquery/issues/2048), [8804644](https://github.com/jquery/jquery/commit/88046440da8f5433b510ea705255d1df12c2963e))
* Remove “#” exception for identifier tokens ([86e62d8](https://github.com/jquery/jquery/commit/86e62d8b37ff9ad40e7c21c2c0c440a9cdfc550e))
* Define jQuery.uniqueSort in selector-native too ([#2466](https://github.com/jquery/jquery/issues/2466), [bf591fb](https://github.com/jquery/jquery/commit/bf591fb597a056bf2fc9bc474010374695b18d1a))
* add test for jQuery.unique() alias ([add85af](https://github.com/jquery/jquery/commit/add85afed5944ec10d68ca10e91421e031fe0a5d))
* add jQuery.uniqueSort; deprecate jQuery.unique ([#2228](https://github.com/jquery/jquery/issues/2228), [e1090c3](https://github.com/jquery/jquery/commit/e1090c3d2b2a988a5b41f1f1ed9f8d6dcae02200))

#### Serialize

* Handle arrays with null values ([3d7ce0a](https://github.com/jquery/jquery/commit/3d7ce0a65f0707ff01a851822e57ba80adcff075))
* Fix object detection ([14c0fe4](https://github.com/jquery/jquery/commit/14c0fe44328f22debb5b531d2b671923658542b3))

#### Sizzle

* update to 2.1.1 ([7602dc7](https://github.com/jquery/jquery/commit/7602dc708dc6d9d0ae9982aadb9fa4615a9c49fa))

#### Support

* Re-organize browser order, add Safari 8 ([43faf6d](https://github.com/jquery/jquery/commit/43faf6d1f922ba44a84c93f4ff2461d208b2bf48))
* Correct iOS 8 support test results, re-arrange entries ([ce308e2](https://github.com/jquery/jquery/commit/ce308e25e57a0a040cd1ea05f00bf1cc23c1bd8a))

#### Tests

* Post-Summit cleanup ([f931786](https://github.com/jquery/jquery/commit/f931786018058174fa63551a7a4a3fccf9de41fa))
* Use standard external domain name ([5b554cf](https://github.com/jquery/jquery/commit/5b554cf04e809d77026d7afba6f02a7599724377))
* Make basic tests work in IE 8 ([5914b10](https://github.com/jquery/jquery/commit/5914b103627e3773418ad1fd8c3b034bf3748d51))
* Don’t load non-basic tests when basic module is selected ([855b0c8](https://github.com/jquery/jquery/commit/855b0c8c288533948b257925a8906f7da3449eed))
* Add simple tests for Android 2.3 ([#2505](https://github.com/jquery/jquery/issues/2505), [2c7e9c9](https://github.com/jquery/jquery/commit/2c7e9c934971500a746d012c529e13ec0b560a83))
* Lower the checks rounding error ([a44cfa0](https://github.com/jquery/jquery/commit/a44cfa00665d21c3197e25c2d63741dc15f6ffb9))
* Use QUnit URL parameter parsing ([f23a64d](https://github.com/jquery/jquery/commit/f23a64d745759d358d423ba0557e8f74d65f76cc))
* more style corrections ([c161eec](https://github.com/jquery/jquery/commit/c161eecce09fc66ce252d4adf64b565f726bb6d2))
* Disable/relax a few tests failing in Android 2.3 ([#1785](https://github.com/jquery/jquery/issues/1785), [1a9c9b0](https://github.com/jquery/jquery/commit/1a9c9b079177a1d6420efb876e8e66bf1fb4cbe2))
* further improvements QUnit 2.0 migration ([c8d15a2](https://github.com/jquery/jquery/commit/c8d15a2f9f108e90d3651c31e4abf45415a30fde))
* fix tests in accordance with new :visible behavior ([16713fb](https://github.com/jquery/jquery/commit/16713fb6097849727de2ba1b489c98e242a168c3))
* hotfix for c1511c673148208ab17cafa0faf37bce3b4ae392 ([3f839af](https://github.com/jquery/jquery/commit/3f839af50b83903279b1f3b614b86c6d4c2b72fc))
* lower the PHP sleep time in unreleasedXHR.html ([02e1008](https://github.com/jquery/jquery/commit/02e10082b25df3b47b6b98e3b35399712795b7df))
* Fix support tests results for Android 2.3 ([4fea389](https://github.com/jquery/jquery/commit/4fea389ad2b7515bc3a9081245979ab7be566b99))
* Add Safari 9 support tests results ([e99a3ac](https://github.com/jquery/jquery/commit/e99a3ac7066226d00ff5828de596d4a4b3818c0c))
* Add dummy modules when running basic tests ([f9af896](https://github.com/jquery/jquery/commit/f9af896bb8f4cb37b22d508443174c8edf40fc54))
* Blacklist the iframe scrollTop test in Opera 12.1x ([283a194](https://github.com/jquery/jquery/commit/283a1949550e1bf1284ddf89a472b3c8b4a97c60))
* do not define two modules with the same name ([#2437](https://github.com/jquery/jquery/issues/2437), [7aa46e0](https://github.com/jquery/jquery/commit/7aa46e0df8a673e6b00550bbbbed21eed50108b7))
* partially use new qunit interface ([#2540](https://github.com/jquery/jquery/issues/2540), [b930d14](https://github.com/jquery/jquery/commit/b930d14ce64937e9478405eee2828d4da091d2cb))
* Correct a typo in the regex matching Safari 8 ([c17543f](https://github.com/jquery/jquery/commit/c17543fd3c14ff86c448dbb90f9fe1223661a73b))
* Change quotes according to style guidelines ([c577928](https://github.com/jquery/jquery/commit/c577928d45bdcc3ee8f93da89ab7aadca21919f3))
* fix lint in restored test ([636a2bd](https://github.com/jquery/jquery/commit/636a2bd4e080f80e3dcc1eb00a5222d8c1eee617))
* Remove a trailing comma for compatibility with the compat branch ([dc8ba6a](https://github.com/jquery/jquery/commit/dc8ba6af921f4c9650fb1e4cfc698b2a276fa53d))
* make editorconfig match css style ([1da1448](https://github.com/jquery/jquery/commit/1da144867f3a49bbac4342bd3f3242baae108eb9))
* make top of the HTML suite compliant with style guide ([8356281](https://github.com/jquery/jquery/commit/8356281bed643bb3d56ad02f52580a0e20dc0237))
* Accept Android 2.3 doesn’t fire window.onerror for remote scripts ([2732531](https://github.com/jquery/jquery/commit/27325311db4807f52d66e592d832c55ab0a203df))
* Add Microsoft Edge results (from Windows 10 build 10130) ([8e111df](https://github.com/jquery/jquery/commit/8e111df641cca3e1b75b31a1971bfc89014b4ded))
* Keep test iframes around for assertions ([0fb84fa](https://github.com/jquery/jquery/commit/0fb84fa8ccefcd07febf282fd7b80262ad70add7))
* Account for array-like objects in jQuery.grep ([67b76f5](https://github.com/jquery/jquery/commit/67b76f5986a78d868553b9aec0d0192f5259a078))
* fix code style issues ([625bd30](https://github.com/jquery/jquery/commit/625bd303d99408bca86b7002cd42b8716e2b267e))
* Fix support tests results ([f6dd767](https://github.com/jquery/jquery/commit/f6dd76709a4173be5e8d45c3f901a330f751c382))
* Account for Edge in originalEvent UA-sniffs ([#2357](https://github.com/jquery/jquery/issues/2357), [64fd7ef](https://github.com/jquery/jquery/commit/64fd7ef3d081b5c65d541237f73a4d89f0f0ad7b))
* Remove Safari 7.0 & iOS 6 support tests results ([47e2aa6](https://github.com/jquery/jquery/commit/47e2aa6593a77c94eef610ac784494884f598253))
* Remove Edge version from the user agent ([5a1217e](https://github.com/jquery/jquery/commit/5a1217e40193c8884155ccaf415091d326ddb52a))
* Tilt at a few style guide windmills ([906caeb](https://github.com/jquery/jquery/commit/906caebb3f3bc542904a94846e778aa8d71c0575))
* Accommodate page changes from the QUnit HTML reporter ([3c13f4c](https://github.com/jquery/jquery/commit/3c13f4c6297566a71102c2362347987f6d6a636e))
* Remove test/data/ua.txt ([#2398](https://github.com/jquery/jquery/issues/2398), [e831856](https://github.com/jquery/jquery/commit/e831856490d2212bdbaff4cd76137b93ccf26d92))
* Minor updates for QUnit 1.16 compatibility ([26276a3](https://github.com/jquery/jquery/commit/26276a307ce2f554b63a05ed8451155f01711c29))
* Update QUnit ([6748ba3](https://github.com/jquery/jquery/commit/6748ba349650353c7bed6eec201a3192f6b2cae1))
* Add iOS 9 support tests results ([1c2b536](https://github.com/jquery/jquery/commit/1c2b5362ef40058d5b375a40362c88559f81a293))
* Fix CSS relative adjustment test for round-down browsers ([48be675](https://github.com/jquery/jquery/commit/48be675200e817f40fa8ec25da1be2ab0839d28d))
* Increase QUnit timeout ([ff18d8e](https://github.com/jquery/jquery/commit/ff18d8e2060ae7c15c7694dc6bcbbeb9cbfbdaa4))
* Expand CSS relative adjustment tolerance for IE ([e22ef5d](https://github.com/jquery/jquery/commit/e22ef5d9017c44cad97ae541fefce76cc455edcb))
* don’t use deprecated argument in test declaration ([aabe94e](https://github.com/jquery/jquery/commit/aabe94edb4880c75eeebc5b5b5d66a9ad17008fe))
* Provide equal() arguments in correct order (actual, expected) ([d3d8d97](https://github.com/jquery/jquery/commit/d3d8d9751f3d14a545b26cf820dc1f51896a7b50))
* Docs: Fix various typos ([03eaadb](https://github.com/jquery/jquery/commit/03eaadb131df925d1072afd2496ee3b41d2f1fc6))
* add the current version of node and iojs to the travis config ([bd9a138](https://github.com/jquery/jquery/commit/bd9a1385feea349f48de658875c3f1bfc75daf74))
* Make regexes for iOS devices more rigid ([015d16c](https://github.com/jquery/jquery/commit/015d16c02dae770eda88e644ec69ce82f25c0412))
* Add .extend test for defined accessor properties ([9748e43](https://github.com/jquery/jquery/commit/9748e436ad80d6a2e1661ba4cf8d7391ed87c3ad))
* Fix Safari 5.1 support tests results ([e904249](https://github.com/jquery/jquery/commit/e904249ee00c3375fad461c47150627fce0b02d8))
* Really fix tests in IE 8 this time ([1b566d3](https://github.com/jquery/jquery/commit/1b566d37a2879af12364a03c633c235a76f49925))

#### Traversing

* Don’t expose jQuery.dir & jQuery.sibling ([#2512](https://github.com/jquery/jquery/issues/2512), [f9ef427](https://github.com/jquery/jquery/commit/f9ef427d355a8a2b531aed5d112dfa4f9692105c))

## 1.12.0

_2016-01-08_ - [blog post](https://blog.jquery.com/2016/01/08/jquery-2-2-and-1-12-released/)

（挺多，慢慢翻译……）

#### Ajax

* Add support comment and fix code style issue ([e38a94a](https://github.com/jquery/jquery/commit/e38a94a61ce92bedf3bed916a042c18a3b5ce4ed))
* remove event dependency from the ajax module ([c580a52](https://github.com/jquery/jquery/commit/c580a529716cd89eccdbda1bf3e9636e5a38811e))
* Fix for request aborted in ajaxSend ([#1775](https://github.com/jquery/jquery/issues/1775), [73c1cea](https://github.com/jquery/jquery/commit/73c1ceaf4280bd0318679c1ad832181f3f449814))
* Fix cross-domain detection test for non-default port ([b635ee2](https://github.com/jquery/jquery/commit/b635ee2d36f2ace7a75239de859da9fd777aa0cd))
* $.post and $.get can now take an options object ([#1986](https://github.com/jquery/jquery/issues/1986), [26150f0](https://github.com/jquery/jquery/commit/26150f0910a0b0d933df92cd354c6735c3dc9078))
* Run the PATCH test only in IE8 on TestSwarm ([#1994](https://github.com/jquery/jquery/issues/1994), [2524da0](https://github.com/jquery/jquery/commit/2524da09c6aa2e3227246ecb1b382bbfe4cead40))
* make jQuery#load “type” field explicit ([1d3d2b1](https://github.com/jquery/jquery/commit/1d3d2b1aa6bcd4de9e3a2d16f98685ac8726311c))
* replace “jqXHR.complete” callback with “always” ([fd80f59](https://github.com/jquery/jquery/commit/fd80f5970f38ff12c7fa2caa8c1de955301a6979))
* move explanatory comment to appropriate place ([04fc801](https://github.com/jquery/jquery/commit/04fc80121756189e1270b1336b4202f99726fa14))
* remove use of jQuery#each second argument ([0877733](https://github.com/jquery/jquery/commit/08777336be849f6241fcb3b5455b5b76af6aae61))
* Use the native XHR for all non-local requests in IE9+ ([#1684](https://github.com/jquery/jquery/issues/1684), [61f812b](https://github.com/jquery/jquery/commit/61f812b7e7b88dd6e0078c241e4c88905ea51562))
* Rename Spartan to Edge in a comment ([8d88cd5](https://github.com/jquery/jquery/commit/8d88cd599f0e9c674eb17c60d528205384c12433))
* Fix the XHR fallback logic for IE8 ([bd699cb](https://github.com/jquery/jquery/commit/bd699cb17b6347a414c0c6d105ef80a4ea1ed678))
* Remove jsonp callbacks through “jQuery#removeProp” method ([#2323](https://github.com/jquery/jquery/issues/2323), [3d850ed](https://github.com/jquery/jquery/commit/3d850edb13b8dfea2c09327f4561ca05cb7dc3bd))
* Account for Android 2.3 not firing window.onerror on script errors ([b3eb2a1](https://github.com/jquery/jquery/commit/b3eb2a13cd51133f56ed3d6755f985cea87a062d))
* do not quote “throws” option – use dot notation instead ([#2571](https://github.com/jquery/jquery/issues/2571), [c530661](https://github.com/jquery/jquery/commit/c530661629ac713a3ccab9691773cc6de5e84759))
* Mitigate possible XSS vulnerability ([#2432](https://github.com/jquery/jquery/issues/2432), [f60729f](https://github.com/jquery/jquery/commit/f60729f3903d17917dc351f3ac87794de379b0cc))
* correct indentation ([2a83417](https://github.com/jquery/jquery/commit/2a8341787acc8519ff49172777c628c28c2c5ec3))
* improve content-type detection ([#2584](https://github.com/jquery/jquery/issues/2584), [3ced5ab](https://github.com/jquery/jquery/commit/3ced5abe5c7e4c90f845012859108059b03770c0))
* don’t expect cross-origin tests run in envs which not support it ([905ab09](https://github.com/jquery/jquery/commit/905ab09afcead6498c1ffc2f82218c51b55352a0))
* Catch synchronous readystatechange events ([#2673](https://github.com/jquery/jquery/issues/2673), [0a6e1c4](https://github.com/jquery/jquery/commit/0a6e1c4b191f177fce2dac5fd3a17b76f853fd26))
* Don’t let onreadystatechange preempt exceptions from xhr.send ([b5c6fc7](https://github.com/jquery/jquery/commit/b5c6fc7ebb3ad83e174211b7858983a8652a774a))

#### Attributes

* fix IE6-7 classes ([9e2f55f](https://github.com/jquery/jquery/commit/9e2f55f47ccc055aafa07d131030ff85e2caa39e))
* don’t test SVG CSS-class manipulation in IE8 ([57fb2dc](https://github.com/jquery/jquery/commit/57fb2dc02ec286c51b456f0e460ad258f332b6ac))
* remove unnecessary element null check ([0de798d](https://github.com/jquery/jquery/commit/0de798d6c2277a286c90e08de669a23e6e12a4a2))
* fix IE8 issues ([f2bcf87](https://github.com/jquery/jquery/commit/f2bcf87c25155fd8361c744c684a0d526bd184a5))
* revert returning null for non-existant attributes ([7bce5b0](https://github.com/jquery/jquery/commit/7bce5b0ee1c8f379477f3276437ed72c59ccda54))
* remove flakey test for selected attribute ([689270e](https://github.com/jquery/jquery/commit/689270e9d8333085ae73144d5a21c244d07c8cb3))
* fix tabIndex on  in IE11 ([#2647](https://github.com/jquery/jquery/issues/2647), [cf4092e](https://github.com/jquery/jquery/commit/cf4092eeea01cd7bc87f1e99e79c3bb2bfcd7d8a))
* revert returning null for non-elements ([a403655](https://github.com/jquery/jquery/commit/a40365549195e4afdf4743f403c12599a3dd4a77))
* add SVG class manipulation ([#2199](https://github.com/jquery/jquery/issues/2199), [b5b0d72](https://github.com/jquery/jquery/commit/b5b0d727740a2e5add2fa0daf0557e1e19a149cb))
* removeClass() -> attr(“class”, “”) ([f5328b6](https://github.com/jquery/jquery/commit/f5328b6a447f23fd8fb9465db36b6eb46e9d8ba6))
* Use simpler boolean check vs a function call ([c003cd6](https://github.com/jquery/jquery/commit/c003cd6bc8336927dad70889ee24e176f90b25a9))
* fix failing test for new return value ([17bd6e9](https://github.com/jquery/jquery/commit/17bd6e9cf94f435807eeb538a47b5e506a01f4cb))
* return null when attribute does not exist ([#2118](https://github.com/jquery/jquery/issues/2118), [afca031](https://github.com/jquery/jquery/commit/afca031826045e9d13454316ec3ec7388225e879))
* Simplify the option val hook; backport a test from master ([#1902](https://github.com/jquery/jquery/issues/1902), [aec41a5](https://github.com/jquery/jquery/commit/aec41a5c41df5a1b9a062950d90babdc0694b084))
* fix toggleClass(boolean) in ie6/7 ([41c83f5](https://github.com/jquery/jquery/commit/41c83f5c016a99b0d3f39d1320799b4c11df22f3))

#### Authors

* Update AUTHORS.txt and .mailmap ([d39fef8](https://github.com/jquery/jquery/commit/d39fef8472e5ca970e77c211d3b116f98fc10b14))

#### Build

* update grunt-jscs-checker and pass with the new rules ([91e06e9](https://github.com/jquery/jquery/commit/91e06e9aebecf67a5c4997408bf0a28fffd03f9d))
* update source map options for the new grunt jshint ([181b451](https://github.com/jquery/jquery/commit/181b451646f518eabb1fb4c0026e74d2f736efd2))
* update requirejs dependency to 2.1.17 ([#2290](https://github.com/jquery/jquery/issues/2290), [a9296df](https://github.com/jquery/jquery/commit/a9296dffb05acab170f1ee76971f85349c804f08))
* denote that sizzle cannot be removed on this branch ([#14775](https://github.com/jquery/jquery/issues/14775), [764f364](https://github.com/jquery/jquery/commit/764f3643a3df30316d642ac6837409e5003859a8))
* Rearrange grunt/npm tasks into a build/dist/test pattern ([0771973](https://github.com/jquery/jquery/commit/07719736b7ead25cdcf511d785ae2591a4d631d3))
* Update the license attribute ([#2331](https://github.com/jquery/jquery/issues/2331), [8bf81d7](https://github.com/jquery/jquery/commit/8bf81d76d1d6d607e0b6b4dd7f5582c3c83637f9))
* append “+compat” to tag version and jQuery.fn.jquery ([#2269](https://github.com/jquery/jquery/issues/2269), [d18b645](https://github.com/jquery/jquery/commit/d18b64578859a6c28e2d4b92e558193f9db9b1d4))
* remove bower.json lint target ([24a6bb9](https://github.com/jquery/jquery/commit/24a6bb9fe8d9ce330056d4e974fb711a6f08c0ad))
* Update grunt-contrib-jshint ([a022da7](https://github.com/jquery/jquery/commit/a022da70568119688445708970bec1346c9d4217))
* Remove npm from dependencies ([a16b77f](https://github.com/jquery/jquery/commit/a16b77fb89c5e6c08d87ce0d042e4620889ded7b))
* Temprary disable jscs checks ([0e3fa47](https://github.com/jquery/jquery/commit/0e3fa47abb48bb5cd627b3f18e4b7f8f39338cc6))
* code style fixes ([8c507df](https://github.com/jquery/jquery/commit/8c507df1d5aad7e9d0b72b96fb8f6b9dcca9ba51))
* Upgrade to commitplease 2.0.0 ([630a5a8](https://github.com/jquery/jquery/commit/630a5a8c0b53dcc419257f6288e6e8b6a0e4c2c3))
* remove needless file and re-enable jscs ([813b7e4](https://github.com/jquery/jquery/commit/813b7e4c8de2d4e5950d279ffdd1c171d529c764))
* update Sizzle ([#2042](https://github.com/jquery/jquery/issues/2042), [#1969](https://github.com/jquery/jquery/issues/1969), [345c95a](https://github.com/jquery/jquery/commit/345c95ae9303ff6a70e27ec5aeb1c9e8e6936e32))
* 1.x-master -> compat ([2912ddd](https://github.com/jquery/jquery/commit/2912ddd824228b200a0d2a1682456ee6827459a5))
* Put “jQuery Compat” in banners in built files ([8cd6875](https://github.com/jquery/jquery/commit/8cd68759352fbec0f1533ef4c491f4fe155c1904))
* Update license ([9dfb9af](https://github.com/jquery/jquery/commit/9dfb9af9624d5b7d03705d34e65b0a610193f192))
* Point to files from the compat branch, not master ([b7663ea](https://github.com/jquery/jquery/commit/b7663eabcd4ff6f56724a3aa2a6b903e4816c208))
* Fix various typos ([3f9fda8](https://github.com/jquery/jquery/commit/3f9fda8fab2a58bb8506553a78d5ecc3c2a67871))
* remove node .10 from travis ([498fd24](https://github.com/jquery/jquery/commit/498fd24f389105049bc2eebadfa43e228b91454a))
* Update native-promise-only (again) ([f9f4f9d](https://github.com/jquery/jquery/commit/f9f4f9d32bd35d374b9fc0d10db8d658475403a6))
* Test on Node 5 ([06840d8](https://github.com/jquery/jquery/commit/06840d8b257f568dd84ea4d54d35ff25702f1e4e))
* code style fixes after all those reverts ([14eba98](https://github.com/jquery/jquery/commit/14eba98c8f189c2e6a36e640bedce2ce6db34493))
* ignore test dependencies for npm install ([ae7a15b](https://github.com/jquery/jquery/commit/ae7a15b780336c95a4784de097ec20cbbe608341))
* Update commitplease dev dependency ([a96ed7e](https://github.com/jquery/jquery/commit/a96ed7e24530a85686d67162ddb294066c5611b0))
* update AUTHORS.txt ([799332f](https://github.com/jquery/jquery/commit/799332fd7ebae2963c176bbcb2f513348e4526ed))
* Upgrade to grunt-bowercopy 1.0.0 ([5150442](https://github.com/jquery/jquery/commit/5150442e1bf4343b28aa69e0f1ad32842533e23a))
* add mailmap entry ([1682d36](https://github.com/jquery/jquery/commit/1682d36be2453007583c3c18d5ebbfa743322ff0))
* just tack on +compat to versions that may include labels ([8565f54](https://github.com/jquery/jquery/commit/8565f54257df78ac0555435b77f121c5bb826ce0))
* Remove unused Sizzle test files ([62f7f7b](https://github.com/jquery/jquery/commit/62f7f7be9bd6cb1f9f85dfa22af29b8a20e6d72a))
* Move all external libraries to external directory ([72e6192](https://github.com/jquery/jquery/commit/72e61925179aac67df234c46b94fcac829142897))
* update Sizzle to 1.11.1 and include license ([1c31384](https://github.com/jquery/jquery/commit/1c3138412ce044d02d714221bea49691a767d41b))
* update grunt-bowercopy ([b3edc61](https://github.com/jquery/jquery/commit/b3edc61c54573e71c34e0397e4737d53f1d9714c))
* Add “timers_ie.js” file back to the repo ([31e6697](https://github.com/jquery/jquery/commit/31e6697c5856ed1d3d79e457dccbf4a1078cb74b))
* Correct indentation issue ([d0f27a7](https://github.com/jquery/jquery/commit/d0f27a73a1917a8c052fc6fc67065f072460ab67))
* Add a comment explaining why the es3 option is needed ([b988c0e](https://github.com/jquery/jquery/commit/b988c0e45d0d876ae7d12e7b361a25a8ea76cf2f))
* Remove empty define({}) from build output ([#1768](https://github.com/jquery/jquery/issues/1768), [2138f15](https://github.com/jquery/jquery/commit/2138f158be66dc2c6c3578dda413908d11aec675))
* bower.json: remove moot `version` field ([3699ef4](https://github.com/jquery/jquery/commit/3699ef463224a08233f9c37c6c7ad8235eb9a758))
* update Sizzle to 2.2.1 ([#2390](https://github.com/jquery/jquery/issues/2390), [20cd343](https://github.com/jquery/jquery/commit/20cd34384d6908e0280cea9b69e09f065c4e4003))
* drop bower; use npm for front-end deps ([#15186](https://github.com/jquery/jquery/issues/15186), [79c0732](https://github.com/jquery/jquery/commit/79c0732ac26253feb6070de409e3643607a5a4c4))
* correct jscs paths ([fa8a5a9](https://github.com/jquery/jquery/commit/fa8a5a90e157f26a54ce50b4e8bb8f2f4bce3500))
* Update jscs and lint files ([#2056](https://github.com/jquery/jquery/issues/2056), [20ddbe4](https://github.com/jquery/jquery/commit/20ddbe4f594f78f7f1095050aabd91882dde0670))
* Add “deprecated” to the Testswarm module list ([b94af72](https://github.com/jquery/jquery/commit/b94af72bc8da4802abab6a5b300fb444dfcacea9))
* remove deprecated JSHint options ([9edd95f](https://github.com/jquery/jquery/commit/9edd95ffd7d4ffadb6893457a738a56d7e4c18d3))
* fix broken assertions caused by QUnit update ([98c77c1](https://github.com/jquery/jquery/commit/98c77c1199660be3116a0663806f5851a3fe3acf))
* space between curly and paren is optional ([#2399](https://github.com/jquery/jquery/issues/2399), [cbb0be6](https://github.com/jquery/jquery/commit/cbb0be6c41221ba3dae280aee07815007b127982))
* update front-end dependencies ([4089c7d](https://github.com/jquery/jquery/commit/4089c7dae46b3a191ae1c075c5e300d5aa3c2d5d))
* fix tests in AMD mode ([57652ee](https://github.com/jquery/jquery/commit/57652eecd96e47f39725671ffce45bfa01493380))
* Update grunt-contrib-uglify because of a security issue in uglify ([2da0cca](https://github.com/jquery/jquery/commit/2da0cca7d364cc8211b10b7fe1868754aba4fca6))
* Update QUnit to latest (1.17.1) ([db31206](https://github.com/jquery/jquery/commit/db31206d36a3a75c011310e282e0fdc9a0f3d99d))
* another portion of code style fixes ([f913a01](https://github.com/jquery/jquery/commit/f913a0131d9843d5f4e267af4268a678944f3e91))
* update node dependencies barring jscs ([511eb15](https://github.com/jquery/jquery/commit/511eb1540bba2fbd45b6399c60ca361f11e572df))
* account for version labels in Sizzle versions ([#1939](https://github.com/jquery/jquery/issues/1939), [ac70dd0](https://github.com/jquery/jquery/commit/ac70dd0c8d6e0953a714519fa7b792b71062b8fb))
* update node dependencies ([dda65fb](https://github.com/jquery/jquery/commit/dda65fb13cce2a75cdaea963e8c1da69ff023358))
* Fixed issue with base path that contain ‘var’ ([#2450](https://github.com/jquery/jquery/issues/2450), [4e3f971](https://github.com/jquery/jquery/commit/4e3f9718666e3cc98b2b149e4b68069c01418db4))
* Sizzle version labels must start with a dash ([6bc0e50](https://github.com/jquery/jquery/commit/6bc0e50810416fe2c2a6c94e28e641aaaeaa16eb))
* Fix an email address of a contributor ([648280a](https://github.com/jquery/jquery/commit/648280a07129205fc1559cfe13fb6108ede9b38c))
* Speed up the Travis build ([ba352e8](https://github.com/jquery/jquery/commit/ba352e83afcb5fca806488a1323b23d409fcbfdd))
* Don’t install jsdom 3 on Node.js 0.10 & 0.12 by default ([#2519](https://github.com/jquery/jquery/issues/2519), [5f1c7fc](https://github.com/jquery/jquery/commit/5f1c7fc81e0ea7bb072268724c0eeed137eb932b))
* Sanctify the component name status of Wrap ([abfb10c](https://github.com/jquery/jquery/commit/abfb10c82ef91fef99ba92c287a6c5a9e8045e80))
* Remove dates from copyright notice ([a0bf5bf](https://github.com/jquery/jquery/commit/a0bf5bf710e98f86a49fc0c293232250f6c40ee1))
* Specify valid components for commit messages ([6f0db53](https://github.com/jquery/jquery/commit/6f0db5319d71261d47157c0a9ac0a2749a7b3311))
* Remove a double empty line at the end of .travis.yml ([fc87a5c](https://github.com/jquery/jquery/commit/fc87a5cd5b2d264dac713ac2d6406d87dd12e674))
* Use double quotes in .travis.yml ([ca0dd7a](https://github.com/jquery/jquery/commit/ca0dd7a3805cdeded88863b696afb72688d1f7b8))
* Drop io.js testing, test on latest Node.js ([d29c394](https://github.com/jquery/jquery/commit/d29c394c1f1f918daef09bfc6def62c0b01b5d2d))
* Move test to appropriate module ([9953ae4](https://github.com/jquery/jquery/commit/9953ae4c88fa2edea2c3dc7ae723912f547f5e29))
* Update native-promise-only ([7b11131](https://github.com/jquery/jquery/commit/7b111310977a30d02a8260a7ed6c9c437bb1b0a5))

#### Callbacks

* Reduce size ([18baae2](https://github.com/jquery/jquery/commit/18baae2efb36a6c759c0dddac7d25da9c554dff7))
* No object starts out locked ([#1989](https://github.com/jquery/jquery/issues/1989), [f5a8c64](https://github.com/jquery/jquery/commit/f5a8c649b54e8b7fde6253bd56972347f9bbe012))
* Disabling a callback should prevent firing ([#1790](https://github.com/jquery/jquery/issues/1790), [61df648](https://github.com/jquery/jquery/commit/61df64865116ea4eac8b4f6da393ba4670f26103))
* Change broken url to wayback one ([e4cbc97](https://github.com/jquery/jquery/commit/e4cbc973d5a5d3b86856fc702f10add36ed0e860))

#### CONTRIBUTING

* Condense info and add directions to other resources ([#1824](https://github.com/jquery/jquery/issues/1824), [404d2aa](https://github.com/jquery/jquery/commit/404d2aa269e87bc952691a2ad833493e3585e543))

#### Core

* Consistently use local reference to access() ([eeab75d](https://github.com/jquery/jquery/commit/eeab75da0048e9708b7bfd1f3e933da7fab050de))
* add support to tag-hyphenated elements ([f19595c](https://github.com/jquery/jquery/commit/f19595cef4a01d52ade451e90b0a1d2ceb5afe43))
* Remove unnecessary parameter to jQuery#constructor ([dc76dca](https://github.com/jquery/jquery/commit/dc76dca295e6413edbac5c9aa0ffadd69a085577))
* Support Symbol wrapper objects in jQuery.type ([c7cf286](https://github.com/jquery/jquery/commit/c7cf28681eeb2a7f6d71e5e17b293c252900bda7))
* simplify “each” stylesheet iteration test ([889bb1e](https://github.com/jquery/jquery/commit/889bb1e3ee56571754793ff98d9dcf4c69fa9581))
* add unit test for isPlainObject(Symbol) ([#2645](https://github.com/jquery/jquery/issues/2645), [d3a2fdc](https://github.com/jquery/jquery/commit/d3a2fdce9773ec688ffe50e94bce9e7f4140ad6a))
* introduce createHTMLDocument in parseHTML; Safari 8/IE8 left out ([828a718](https://github.com/jquery/jquery/commit/828a718aa028ba6cde7b4076d94b10ef0853f9ee))
* change jQuery.each and jQuery#each signatures ([#2090](https://github.com/jquery/jquery/issues/2090), [7cd9a36](https://github.com/jquery/jquery/commit/7cd9a363229c6ec1ceaa4debf49ee3eb20d97761))
* remove isArraylike check for nodes ([#2238](https://github.com/jquery/jquery/issues/2238), [d693391](https://github.com/jquery/jquery/commit/d6933917d217321e3d505abe201f3bf5bf7c3d66))
* Simplify and speed up .each ([4cc4e54](https://github.com/jquery/jquery/commit/4cc4e54298bca84d0a0b2f2eb1ee97ca619485b1))
* Support non-browser environments ([#2133](https://github.com/jquery/jquery/issues/2133), [#2501](https://github.com/jquery/jquery/issues/2501), [04ec688](https://github.com/jquery/jquery/commit/04ec688e806660107a0b5823fabe2fe213f63b92))
* CSS: Attach test nodes to documentElement, not body ([#2502](https://github.com/jquery/jquery/issues/2502), [9b04201](https://github.com/jquery/jquery/commit/9b04201ff21b6e5932dc21679774f398d6940cfa))
* make isNumeric test work on Symbol ([d846c25](https://github.com/jquery/jquery/commit/d846c25dca4adeb4262f98957f1b887fe6b29912))
* Don’t expose jQuery.access ([#2513](https://github.com/jquery/jquery/issues/2513), [12230d3](https://github.com/jquery/jquery/commit/12230d39e1e897d5edfaad846650a535c578c992))
* Adjust comments & tests after dropping Safari 6 support ([5fce498](https://github.com/jquery/jquery/commit/5fce498e4263f11ed4c688e5304999e63c395367))
* .each/.map should accept an undefined/null value ([#2267](https://github.com/jquery/jquery/issues/2267), [15f4804](https://github.com/jquery/jquery/commit/15f48047bcf01389643e1561de9907c417529e83))
* Add a support comment for Safari 8 ([9c373c3](https://github.com/jquery/jquery/commit/9c373c31410deb8e4a11aa7ce226d5e9169c7852))
* Make jQuery objects iterable ([#1693](https://github.com/jquery/jquery/issues/1693), [2fa3bac](https://github.com/jquery/jquery/commit/2fa3bac7eb2021361a1d0c498c278df812ec48b9))
* Align code in intro.js with master ([fe2a584](https://github.com/jquery/jquery/commit/fe2a584ed662ad15e0cfb2e806652e2a8724f0c8))
* Update tested jsdom, drop obsolete workarounds ([#2153](https://github.com/jquery/jquery/issues/2153), [19c0377](https://github.com/jquery/jquery/commit/19c0377fcc92a765c8a15ce68119f52fad2aae1b))
* Standardize indexOf comparisons ([6ae222a](https://github.com/jquery/jquery/commit/6ae222a54f687e7950a3f4c4e04bd42ca0387504))
* Drop strundefined variable ([835e8c4](https://github.com/jquery/jquery/commit/835e8c4ae39f09d11ad42d24e0210bebfa8e8320))
* organize prop & attr code to be similar ([d0388e9](https://github.com/jquery/jquery/commit/d0388e9e806ca3b30e7bbaaa1c336b7c98dc5f88))
* Change support.ownLast to support.ownFirst ([#2406](https://github.com/jquery/jquery/issues/2406), [453738a](https://github.com/jquery/jquery/commit/453738ab85600d8f8201fcf89e40b68f076c5cbd))
* Follow the AMD specification for define ([acf2d0c](https://github.com/jquery/jquery/commit/acf2d0c36b16fc85e8236776f1254a8886b32da0))
* add workaround for iOS JIT error in isArrayLike ([#2145](https://github.com/jquery/jquery/issues/2145), [1e7a2f3](https://github.com/jquery/jquery/commit/1e7a2f3674d4bc62ba6cc537e42b2e417a9c5ba6))
* CSS:Event: simplification of native method signatures ([49bce47](https://github.com/jquery/jquery/commit/49bce4712447a73ae60268f34d067cdf88a070bb))
* allow init to accept an alternate rootjQuery for migrate’s sake ([#2101](https://github.com/jquery/jquery/issues/2101), [c916aef](https://github.com/jquery/jquery/commit/c916aef84f12843d20c4e39d89e79cccd2547950))

#### Css

* Fix the “sanity check” test ([da84cb6](https://github.com/jquery/jquery/commit/da84cb6b7aa48f12d98103d40e0621ceab2b7935))
* Remove non-functional unit test for negative margin ([1ece10f](https://github.com/jquery/jquery/commit/1ece10fbeeccc92d5860e7c4de3dcbae67c17e76))

#### CSS

* Add a support test for the hack for .css(‘marginRight’) etc. ([25bc680](https://github.com/jquery/jquery/commit/25bc6809c56026aa4f21dbb73eb950ba2677eb21))
* fix :visible/:hidden selectors for inline element w/ content ([#2227](https://github.com/jquery/jquery/issues/2227), [dd816db](https://github.com/jquery/jquery/commit/dd816dbac19d8a83f9b1e9c7d09bc0db436a74b0))
* fix AMD mode for the new showHide module ([0b6846c](https://github.com/jquery/jquery/commit/0b6846c6b77b0f810c42021090154e1910de135a))
* fix visible/hidden for IE6/7 ([ecf52b9](https://github.com/jquery/jquery/commit/ecf52b948bcc7c9a28b5b2f93a0764868f09428e))
* use isFinite in place of redundant isNumeric ([24ab836](https://github.com/jquery/jquery/commit/24ab83659e3565642aac0f487ef555112601ed2b))
* Protect against getBoundingClientRect exceptions ([c40b12a](https://github.com/jquery/jquery/commit/c40b12a6bd30649066babc6f8c16b53a14b110dd))
* elements are hidden when either offsetWidth or offsetHeight is zero ([#10406](https://github.com/jquery/jquery/issues/10406), [#13132](https://github.com/jquery/jquery/issues/13132), [7b9b98d](https://github.com/jquery/jquery/commit/7b9b98d6e3f5a72089fa53b0f32f6f1e54abaa29))
* Add an integration test for issue gh-1764 ([7ee0fea](https://github.com/jquery/jquery/commit/7ee0feaca65f37780aac4924705a0ec37c56094e))
* Don’t name the anonymous swap function ([e847574](https://github.com/jquery/jquery/commit/e847574fc755b5339f3de41bcebd5b2a3e140cfe))
* Fix the pixelMarginRight support test in IE8 ([4a67512](https://github.com/jquery/jquery/commit/4a67512f8bfb1b7b19837fb1f8920a33061933e3))
* Improve a comment explaining IE11 fullscreen bug ([5895340](https://github.com/jquery/jquery/commit/589534008873c4c083d14b07cc36c9b2ae4c5399))
* Removed redundant “to the number” in comment ([b59b819](https://github.com/jquery/jquery/commit/b59b819ffec6e2b3171625e45d33e61ff7b9dbfe))
* Fix get upper case alpha opacity in IE8 ([#1705](https://github.com/jquery/jquery/issues/1705), [c5e8e12](https://github.com/jquery/jquery/commit/c5e8e12cef31fee89965891669ecdca6436be319))
* Support relative adjustment in any applicable unit ([#1711](https://github.com/jquery/jquery/issues/1711), [6fb2cef](https://github.com/jquery/jquery/commit/6fb2cefc602cf8bd8b85373f480e978bb8978e37))
* make the getStyles function more readable ([bf282ea](https://github.com/jquery/jquery/commit/bf282ea8e20892af2d1d2c76b93b0c1f2141db97))
* Add animation-iteration-count to cssNumber, fix tests ([#2792](https://github.com/jquery/jquery/issues/2792), [01fb17b](https://github.com/jquery/jquery/commit/01fb17be63d3d08789303f2e0eb7b6fcccc8fd56))
* Work around an IE11 fullscreen dimensions bug ([#1764](https://github.com/jquery/jquery/issues/1764), [6df1bf9](https://github.com/jquery/jquery/commit/6df1bf9be818b8955f94113aecc689fdf7a2e172))
* remove revert artefact ([fc6ac9d](https://github.com/jquery/jquery/commit/fc6ac9d1d5240c098998ded476582e36b284212e))
* Don’t expose jQuery.swap ([#2058](https://github.com/jquery/jquery/issues/2058), [02a9d9f](https://github.com/jquery/jquery/commit/02a9d9f94b623ea8664b7b39fd57feb7de6c6a14))
* Correct typo in the comment ([787ffbf](https://github.com/jquery/jquery/commit/787ffbf5fa9a1afb5883edc576e954337b069bb6))
* Remove use of getDefaultComputedStyle ([44c9c4f](https://github.com/jquery/jquery/commit/44c9c4f7519adb0b8c676251e67f4de0dc2a5276))
* Don’t cache unrecognized CSS property names ([#2015](https://github.com/jquery/jquery/issues/2015), [42ea746](https://github.com/jquery/jquery/commit/42ea7468250f1b612684a71b8643ae25367ff469))
* Correct misrepresentation of “auto” horizontal margins as 0 ([#2237](https://github.com/jquery/jquery/issues/2237), [214e163](https://github.com/jquery/jquery/commit/214e1634ab9b1d13d53647dd5de3bdf7a091d49c))
* fix reliableHiddenOffsets support test for IE6-7 ([77f9b1e](https://github.com/jquery/jquery/commit/77f9b1e8037b1e4dc12e64cf10240f4b97383c30))
* fix dependency order for amd ([e185aa3](https://github.com/jquery/jquery/commit/e185aa3f06a0da69dc001b81425354b9c05e40fd))
* Use pre-defined displays for html and body ([b05b6a2](https://github.com/jquery/jquery/commit/b05b6a22197009d589e478f77e1dfebf43c6ffc4))
* Add unit tests for negative margins and positioning ([ae30fb6](https://github.com/jquery/jquery/commit/ae30fb6c27a2121578d3ce7ca6e2ba1d205545b8))
* Clean up memory leak in reliableMarginRight ([#1795](https://github.com/jquery/jquery/issues/1795), [fa70df6](https://github.com/jquery/jquery/commit/fa70df692eff16ad5d64a65ec565542d0690f732))

#### Data

* Use a PDF object instead of a Java applet for acceptData testing ([#1938](https://github.com/jquery/jquery/issues/1938), [4e3c48f](https://github.com/jquery/jquery/commit/4e3c48f239f0ed265a53a33dfda1ba7dc6223db4))
* Don’t expose jQuery.acceptData ([#2555](https://github.com/jquery/jquery/issues/2555), [bec2ba2](https://github.com/jquery/jquery/commit/bec2ba231288ec4abba63c3a5ca8ad26715a318b))
* use removeAttribute in cleanData to bypass Chrome bug ([#1664](https://github.com/jquery/jquery/issues/1664), [9d1d90e](https://github.com/jquery/jquery/commit/9d1d90e7a274cae7f5f587bd28613044ea24264f))
* backport cleanData tests from gh-2480 ([624d6a8](https://github.com/jquery/jquery/commit/624d6a8580a7e1108c81a6a777dc1be3d408bddf))
* test that delete is not used on DOM nodes ([5a7674d](https://github.com/jquery/jquery/commit/5a7674d6356c1d8c8a485e1739db1c3ae087f9d1))

#### Deferred

* pass lint in new catch tests ([203979d](https://github.com/jquery/jquery/commit/203979d15391877c1d8ca2674e89dd16cba95029))
* Always handle progress callbacks before done/fail ([#2013](https://github.com/jquery/jquery/issues/2013), [#2010](https://github.com/jquery/jquery/issues/2010), [35295f1](https://github.com/jquery/jquery/commit/35295f1c20d6f4ce724840ecad00d347ca5a1295))
* Fix $.when with resolved deferred and progress callbacks ([efb98f8](https://github.com/jquery/jquery/commit/efb98f85bab7f2ec9f38d6991d7b1bc683a514ce))

#### Deprecated

* fix amd mode for the deprecated module ([bd11778](https://github.com/jquery/jquery/commit/bd11778168e5d96b513a03015864aa0fc9536acb))

#### Dimensions

* allow modification of coordinates argument ([1eedf0e](https://github.com/jquery/jquery/commit/1eedf0e9ea4dc2d12edf28e77b33ae23de01af3b))

#### Docs

* Rename 1.x to compat ([8992ac8](https://github.com/jquery/jquery/commit/8992ac86cc4b8321177426c8b1bc7a1842bbfa45))
* remove redundant instruction from the readme ([#2359](https://github.com/jquery/jquery/issues/2359), [e6a492d](https://github.com/jquery/jquery/commit/e6a492d3b6a1b219a36ef1485c1e1a06967c26e7))
* correct grunt command in README.md ([38ac3c4](https://github.com/jquery/jquery/commit/38ac3c43ffdd79e6d8fd6ef5d652228fbc5ac33f))
* Clarify custom build instructions ([8e738f0](https://github.com/jquery/jquery/commit/8e738f0aa89ca333dac61a1d1d0c4964762464c1))
* Fix various spelling mistakes ([6af92ca](https://github.com/jquery/jquery/commit/6af92cafcadba74c22b8d94779472e1f71b99e30))
* 1.x-master branch -> compat branch; 2.x branch -> master branch ([b8a0843](https://github.com/jquery/jquery/commit/b8a084374cc51aa6060e121e6bdc0e1f3ceb3576))
* “npm run build” was missing from the contributing guides ([5da5035](https://github.com/jquery/jquery/commit/5da5035039c48fd00e3effa5135e257ccda79454))

#### Effects

* Finish should call progress ([#2283](https://github.com/jquery/jquery/issues/2283), [f71e32d](https://github.com/jquery/jquery/commit/f71e32d4b46f3be293304d40ed6dc85cf30d6a7b))
* Add tests for jQuery.Tween ([6b10f9d](https://github.com/jquery/jquery/commit/6b10f9d7e9fb6d062d2bbda49196544cd059b05c))
* Remove tests for jQuery.Animation & jQuery.Tween ([bc53033](https://github.com/jquery/jquery/commit/bc53033080f1b3ea47ce722d6e375ac44e8f694d))
* add tests for jQuery.easing._default in Animation and Tween ([b9b5c23](https://github.com/jquery/jquery/commit/b9b5c23fd74c2d3786739c9e6911c811c56a205e))
* set default easing using jQuery.easing._default ([#2219](https://github.com/jquery/jquery/issues/2219), [b7f9e62](https://github.com/jquery/jquery/commit/b7f9e62642f4534329bf473861c7737669b1e8c4))
* Remove needless operations in tests ([13040b6](https://github.com/jquery/jquery/commit/13040b655a33543c5d8f2142678faebfa10b37bc))
* add back support.shrinkWrapBlocks() for ie6 ([1f85ded](https://github.com/jquery/jquery/commit/1f85ded20444ab9b1c48ff33bfaa00668941e98b))
* fix failing tests in IE8 ([fe6afa8](https://github.com/jquery/jquery/commit/fe6afa8268e01f36bb0d1b88c13d704560039c3f))
* Fix tests ([29561bc](https://github.com/jquery/jquery/commit/29561bca8f33f4bf03a7186eb9c38a3cb18a8993))
* Adding unit tests for jQuery.Animation ([0ff8057](https://github.com/jquery/jquery/commit/0ff805772ad046ff1e9ecf1f9958408ce0cfcfcd))

#### Event

* Use form prop so that a propHook can be used ([#2332](https://github.com/jquery/jquery/issues/2332), [ead83b9](https://github.com/jquery/jquery/commit/ead83b9c8a6b751f31f0197ff0364e95a1ca24cd))
* improve originalEvent hack ([37c3d08](https://github.com/jquery/jquery/commit/37c3d087824b51e742126252ced8be592858102d))
* Remove an internal argument to the on method ([473d2db](https://github.com/jquery/jquery/commit/473d2db9fdf2dbbef260da82fcb80b2e050132d0))
* Empty namespaces should be uneventfully ignored ([51564bb](https://github.com/jquery/jquery/commit/51564bbd39506d2076a5c82bdf87db92e81c26c9))
* fix incorrect test ([e73a67f](https://github.com/jquery/jquery/commit/e73a67f2e214a1fe3f628b3eed7bc4a3bdbe6d18))
* add test for window scrollTop/Left logic in iframes ([2c14b00](https://github.com/jquery/jquery/commit/2c14b00a863278bbee9817a2fd5e7f72560477a0))
* Move .bind() and .delegate() to deprecated ([#2288](https://github.com/jquery/jquery/issues/2288), [7e78c2e](https://github.com/jquery/jquery/commit/7e78c2ec81dbb7bac9222864c4981ed0a54b66e5))
* Add reference to data module ([2866da9](https://github.com/jquery/jquery/commit/2866da9e12b7cf339667ae894ffe072f4eb673de))
* Normalize mouse event properties in drag events ([#1925](https://github.com/jquery/jquery/issues/1925), [5b0b1b7](https://github.com/jquery/jquery/commit/5b0b1b77dbc41c144959ef2fe8de603555beb39b))
* HTML5 drop events inherit from MouseEvent ([#2009](https://github.com/jquery/jquery/issues/2009), [a05de40](https://github.com/jquery/jquery/commit/a05de404d8459752a34bf65297df5ac780bac554))
* Add a note about a mouseenter bug in Chrome ([f3e3a20](https://github.com/jquery/jquery/commit/f3e3a208dedd24072ab15361a925e60c997bbb2d))
* provide verbose info for focus(in | out) & rename support props ([401a351](https://github.com/jquery/jquery/commit/401a351bd25f396099f26d71ea610c30b2d498a8))
* Restore the `constructor` property on jQuery.Event prototype ([#15090](https://github.com/jquery/jquery/issues/15090), [d4a998f](https://github.com/jquery/jquery/commit/d4a998f62fde4b9347b99571a7d000b53731909a))
* correct support comment ([fae2daa](https://github.com/jquery/jquery/commit/fae2daadaa2039aa3b683416e49c664d499ea6fd))
* Reduce differences from master ([3923bb8](https://github.com/jquery/jquery/commit/3923bb8400b149f483b7115d0edd2f304348b189))
* remove preDispatch hook & simplify “simulate” signature ([05e54ce](https://github.com/jquery/jquery/commit/05e54ce798cbb1a8b357e000cc9d691f7bb6c616))
* add support comment ([0fc5beb](https://github.com/jquery/jquery/commit/0fc5bebb63decb57dfe4247ea836fbf402d92ad1))
* Reduce differences from master ([e4c5f87](https://github.com/jquery/jquery/commit/e4c5f878511f10710e5231848036b992cf49c380))
* Update support comments for mouseenter/mouseleave implementation ([d176001](https://github.com/jquery/jquery/commit/d176001e6e4f0dda877ae17f56277f9ec8e30c9a))
* Copy detail property to jQuery.Event on native events ([#1867](https://github.com/jquery/jquery/issues/1867), [a90ff8c](https://github.com/jquery/jquery/commit/a90ff8c8c79bfcc32afd340a12f016f20a31d8b6))
* correct an unfinished comment ([ac23f91](https://github.com/jquery/jquery/commit/ac23f91cbedcdcd20284485baaaf68be4b7f7436))
* Fix delegated radio events when arrow keys are used ([#2343](https://github.com/jquery/jquery/issues/2343), [657c2f8](https://github.com/jquery/jquery/commit/657c2f818075111684ff8e0406dbb74f2b8cdc21))
* Fully clean up events in unit test ([ef93f95](https://github.com/jquery/jquery/commit/ef93f9545263f3ed456367506ac7226c921cd243))

#### Manipulation

* re-expose domManip until 3.0 ([#2225](https://github.com/jquery/jquery/issues/2225), [95de105](https://github.com/jquery/jquery/commit/95de105778c2865e90984eed62e83ed790701170))
* increase delay of data-URI test ([30ace26](https://github.com/jquery/jquery/commit/30ace26c42954497e44f19e8c7fa100de45c489e))
* support data-URI scripts insertion ([bc1902d](https://github.com/jquery/jquery/commit/bc1902ddc08502d60ee77e00ea95d454666d7e56))
* don’t test data-URI with script element in IE8 ([503e545](https://github.com/jquery/jquery/commit/503e54564a8a88b7e968b64a920f2eeceffb0b74))
* Detect sneaky no-content replaceWith input ([#2204](https://github.com/jquery/jquery/issues/2204), [4cafb58](https://github.com/jquery/jquery/commit/4cafb58ba43a85c1870b1ac6b233af262514997e))
* privatize internal domManip() function ([#2225](https://github.com/jquery/jquery/issues/2225), [590eff6](https://github.com/jquery/jquery/commit/590eff6397e830454d2ecf734da7f995a1b89492))
* Plug an IE8 memory leak in noCloneEvent feature detect ([#1840](https://github.com/jquery/jquery/issues/1840), [faf295a](https://github.com/jquery/jquery/commit/faf295a6d85ea716bd795609efdd855938144512))
* Make an HTML interception point ([#1747](https://github.com/jquery/jquery/issues/1747), [fb25bac](https://github.com/jquery/jquery/commit/fb25bacf9b809a08c29e76decd8cda1579fdf192))
* privatize buildFragment() function ([#2224](https://github.com/jquery/jquery/issues/2224), [63c1414](https://github.com/jquery/jquery/commit/63c1414a54188685a0bf15ef000cbf5ad75626a6))
* improve test for data-URI ([a467f86](https://github.com/jquery/jquery/commit/a467f8653a6fab2903148df80ab0ce9f5f4fd04f))
* Update html5shiv elements ([#15241](https://github.com/jquery/jquery/issues/15241), [a953389](https://github.com/jquery/jquery/commit/a9533893b9e5e9a248139f5794c5d6099382cf14))
* correct wrapMap assign ([a5be90f](https://github.com/jquery/jquery/commit/a5be90fb293e329500bb13ccd979161dddfcd075))
* Remove an internal argument to the remove method ([#2301](https://github.com/jquery/jquery/issues/2301), [b819be3](https://github.com/jquery/jquery/commit/b819be3e2f35ae64abc26ff9a2fe944e1ffbb7e0))
* Don’t provide the parser with sloppy table markup ([#2493](https://github.com/jquery/jquery/issues/2493), [81b6e46](https://github.com/jquery/jquery/commit/81b6e46522d8c680f6c38d5e95c732b2b47130b9))
* Switch rnoInnerhtml to a version more performant in IE ([#2563](https://github.com/jquery/jquery/issues/2563), [29266e0](https://github.com/jquery/jquery/commit/29266e00e91b2ad42793f7c12965662917d8fce4))
* add support to tag-hyphenated elements ([5d522f5](https://github.com/jquery/jquery/commit/5d522f5c740f1f919a630a5f6ec3d40fad840ff7))
* blacklist IE8 from running tests for tag-hyphenated elems ([87bb713](https://github.com/jquery/jquery/commit/87bb713cc0e5b5aca86b6839894e9f3d8d635b36))

#### Misc

* Mac OS is now OS X, thanks @xfq ([598946d](https://github.com/jquery/jquery/commit/598946d09f5cd9df8575c615a57a9d546a95257a))
* Need for speed removed by 9ad6e7e ([519d99a](https://github.com/jquery/jquery/commit/519d99a1c3c5713d2905f1b07c2f52af277001fb))
* Update all references to bugs.jquery.com ([#1681](https://github.com/jquery/jquery/issues/1681), [49c720e](https://github.com/jquery/jquery/commit/49c720e16a7181a491f7561c2051f42c7b811709))

#### Offset

* return before getBoundingClientRect to avoid error in IE8-11 ([25e8620](https://github.com/jquery/jquery/commit/25e8620da9c6e245516d8ac1b0f9ddc896838883))
* fix iframe scrollTop/Left test for IE8 ([d632699](https://github.com/jquery/jquery/commit/d632699c6b2b1b06dd7cbdec982d930f59fd8119))
* fix iframe scrollTop/Left test for IE8 and iPhone ([62a333e](https://github.com/jquery/jquery/commit/62a333e0646d3011377ed13a6fcfbb08e91e2bef))
* Round offset value for the sake of floating errors ([#2147](https://github.com/jquery/jquery/issues/2147), [cd63e9c](https://github.com/jquery/jquery/commit/cd63e9c622b82a110d8453cc9a128fcf9ea6ade4))
* don’t run scrollTop/scrollLeft iframe test in Android 2.3 & 4.0 ([#1981](https://github.com/jquery/jquery/issues/1981), [f2ea60c](https://github.com/jquery/jquery/commit/f2ea60cfe88f3aa74aed1bccac60ed15929e23e8))
* return zeros for disconnected/hidden elements ([#2310](https://github.com/jquery/jquery/issues/2310), [63f19a9](https://github.com/jquery/jquery/commit/63f19a95b9bfffdc7b8800f89a9def768cc3aebd))
* account for scroll when calculating position ([#1708](https://github.com/jquery/jquery/issues/1708), [0654711](https://github.com/jquery/jquery/commit/0654711e0d929187249ca9507ae5881c72947843))
* do not run tests which break without back-incompat change ([9f2dcb9](https://github.com/jquery/jquery/commit/9f2dcb93f848a698602cb7cde1128e7e6907d9cc))
* getBounding doesn’t return width/height in IE8\. Fixes test. ([3b1de11](https://github.com/jquery/jquery/commit/3b1de112675a5c39410f3ba18c433a6ee4bd4e17))
* no need to check for ownerDocument ([523de77](https://github.com/jquery/jquery/commit/523de777f933d3f50cdf1fe7473a23a368aedcad))
* revert to jQuery.contains for IE8’s sake (compat only) ([6df3990](https://github.com/jquery/jquery/commit/6df399073c6027608dff84bbd3b71e62df6c1c9b))
* allow small differences in offset.top ([#2590](https://github.com/jquery/jquery/issues/2590), [d047073](https://github.com/jquery/jquery/commit/d047073d2bc4f507ed98c157739b1e3d0417b3f6))
* add tests for hidden elements + scroll ([a0a5c0b](https://github.com/jquery/jquery/commit/a0a5c0be2def09f8d380a69d8e6f000169123990))

#### Readme

* Fix punctuation in tile ([a751bfe](https://github.com/jquery/jquery/commit/a751bfe6724e2e5f667f91538ef4f2d10344e997))

#### README

* various text fixes ([3d77c2e](https://github.com/jquery/jquery/commit/3d77c2ee1ee49975af47b3371c09a8ae77d93c15))
* update the Homebrew site address ([d588c85](https://github.com/jquery/jquery/commit/d588c852f06d3a2731aebd038f16e9e3206b399d))
* Improve build instructions ([07afc28](https://github.com/jquery/jquery/commit/07afc284bcb46881727230700f39e12d5f3fb96d))
* Update the description of the deprecated module ([2a3018c](https://github.com/jquery/jquery/commit/2a3018cec9154189ea4317e259390864ce8d81cd))

#### Release

* ensure files are copied to dist ([f5029f5](https://github.com/jquery/jquery/commit/f5029f586aa7ee8478817778cda1f0aabf673f70))
* fix CDN archive creation ([#1940](https://github.com/jquery/jquery/issues/1940), [7352216](https://github.com/jquery/jquery/commit/7352216ca83e0233d2a5ec2fc4ed6583e7bfdbf1))
* remove sourcemap comment from all copies of minified file ([#1707](https://github.com/jquery/jquery/issues/1707), [f71d7f5](https://github.com/jquery/jquery/commit/f71d7f56e96480d2115bff5542ded04ce6546ec9))
* push dist to same remote as project ([5e5489c](https://github.com/jquery/jquery/commit/5e5489cea5e1f4469219e1e3e1ca76c16ba20030))
* Distribute files to distribution repo ([#1869](https://github.com/jquery/jquery/issues/1869), [#1673](https://github.com/jquery/jquery/issues/1673), [#2045](https://github.com/jquery/jquery/issues/2045), [fc76a97](https://github.com/jquery/jquery/commit/fc76a97b990508cc612c5cf805e62fc6e8bfae18))
* update AUTHORS.txt ([ce4822c](https://github.com/jquery/jquery/commit/ce4822c046c154b92e0c46b8e51395a611f9f47b))
* compat -> 1.x. Remove compat-specific release semantics ([25d0afa](https://github.com/jquery/jquery/commit/25d0afa51e08c00556c9e6906851d771a851ae23))
* update AUTHORS.txt ([8b0618c](https://github.com/jquery/jquery/commit/8b0618c295c2b8c509e5f6a27f82c4e3a7f47826))
* update AUTHORS.txt again ([0398d90](https://github.com/jquery/jquery/commit/0398d903719b493e80f5098cc4383c94e9d94343))
* properly set the dist remote when it’s a real release ([9162122](https://github.com/jquery/jquery/commit/9162122ba80e507eb02568761252fcea30391104))
* Remove copying of jquery-latest files ([16fcc5e](https://github.com/jquery/jquery/commit/16fcc5e9e2e6daa42661527dc69311230b5c5044))
* dist can be run during a test ([dcd2c8f](https://github.com/jquery/jquery/commit/dcd2c8f3e37d7fe47420b1b95d75e7a0c957abde))
* allow local and github dists ([3a4a95c](https://github.com/jquery/jquery/commit/3a4a95c7b62cd86dad7c0b47df073f6c44ae6dec))

#### Selector

* add test for jQuery.unique() alias ([17ce9ed](https://github.com/jquery/jquery/commit/17ce9edf1e60f14983b4ff970c9511689c876d5c))
* Remove “#” exception for identifier tokens ([41f522a](https://github.com/jquery/jquery/commit/41f522ace1518f7f6f22f2e227350b0bdf78e62b))
* add jQuery.uniqueSort; deprecate jQuery.unique ([#2228](https://github.com/jquery/jquery/issues/2228), [d9d930f](https://github.com/jquery/jquery/commit/d9d930f79e9e4edb7339199cd758dc654e053a3b))

#### Serialize

* Handle arrays with null values ([f0b86ec](https://github.com/jquery/jquery/commit/f0b86ec050305ac1fbddd4943361b423d86feb4b))
* Fix object detection ([a993056](https://github.com/jquery/jquery/commit/a9930565f157df4bcae63c108aeb9f4825c7314a))

#### Sizzle

* update 2.1.1 ([238bc32](https://github.com/jquery/jquery/commit/238bc32a11a3299bcd350848b976a1cae8c9e781))

#### Support

* Correct iOS 8 support test results, re-arrange entries ([a4e31a8](https://github.com/jquery/jquery/commit/a4e31a8e2c214e4a021856b44a23368d103c169d))
* Re-organize browser order, add Safari 8 ([7e70867](https://github.com/jquery/jquery/commit/7e7086780507946e83cc9837bfb5d951b6eafb00))

#### Test

* Switch leftover andSelf to addBack ([2ea57c1](https://github.com/jquery/jquery/commit/2ea57c1002c877c2771955932bff053c47831779))

#### Tests

* Expand CSS relative adjustment tolerance for IE ([9d255b3](https://github.com/jquery/jquery/commit/9d255b3e50ef2fce9c4f96cb3a3b2c4e71e63068))
* Post-Summit cleanup ([a93d1d7](https://github.com/jquery/jquery/commit/a93d1d7d78a38be8d2c40d615f56f823c660e0ae))
* Add iOS 9 support tests results ([dec9ab9](https://github.com/jquery/jquery/commit/dec9ab9d3fe29686b8922e978ebf1504becc85e9))
* Remove Safari 7.0 & iOS 6 support tests results ([602c34d](https://github.com/jquery/jquery/commit/602c34d45bf3cdc71b2f7e1344b75dc1489dd870))
* Make regexes for iOS devices more rigid ([8339185](https://github.com/jquery/jquery/commit/83391859bda90f630bf02a5e04d82e9f1babeb1f))
* Do not define two modules with the same name ([#2437](https://github.com/jquery/jquery/issues/2437), [85aed35](https://github.com/jquery/jquery/commit/85aed35cb50703e3252cac2e4195baf2f1830c55))
* lower the PHP sleep time in unreleasedXHR.html ([eac265c](https://github.com/jquery/jquery/commit/eac265ccdd4ed51a8fb232f6a4568b6c055f65c1))
* Add dummy modules when running basic tests ([5fb689d](https://github.com/jquery/jquery/commit/5fb689debcab0e9b0969d595b03b911d974eca1f))
* fix code style issues ([8cac6da](https://github.com/jquery/jquery/commit/8cac6da55d78de0f0901927fa20ad70759938a71))
* Account for array-like objects in jQuery.grep ([6e466af](https://github.com/jquery/jquery/commit/6e466af010c8265b3fb3dd73ff5fa7f66d8de8ad))
* Docs: Fix various typos ([ef6cd83](https://github.com/jquery/jquery/commit/ef6cd83ab04d96b8ed9487ee57707100d97bf18c))
* fix support tests in ie9 ([729c75f](https://github.com/jquery/jquery/commit/729c75f4ff2c9e096d367497913fa0c865a21029))
* Account for Edge in originalEvent UA-sniffs ([#2357](https://github.com/jquery/jquery/issues/2357), [4c3e63b](https://github.com/jquery/jquery/commit/4c3e63b47ca78a761d5408c48bd921cde97d8d4c))
* Fix the expando-removal test failure in IE 8 ([#2596](https://github.com/jquery/jquery/issues/2596), [4b1cff6](https://github.com/jquery/jquery/commit/4b1cff65ce6014f7d35f33d222bddd67f74a6f8d))
* make top of the HTML suite compliant with style guide ([bc9e573](https://github.com/jquery/jquery/commit/bc9e573651d99626d2c8faa3f0ef204a6178dddf))
* Add Safari 9 support tests results ([99f41c2](https://github.com/jquery/jquery/commit/99f41c23fd9ba20ea1a18da3cc20f2cffb31c614))
* Provide equal() arguments in correct order (actual, expected) ([4503a61](https://github.com/jquery/jquery/commit/4503a61ff10af737d385168479392a09fd63f7f5))
* do not create data cache when fetching single property ([0874096](https://github.com/jquery/jquery/commit/087409679716f85fff6fa497a3b7efd1620e31ec))
* Increase QUnit timeout ([c0a0777](https://github.com/jquery/jquery/commit/c0a07778fd3a1f6c91fda67916ad492553ef2282))
* Really fix tests in IE 8 this time ([1b48eef](https://github.com/jquery/jquery/commit/1b48eef4caf7fa3aba0ee1a3473e0d46487d20ea))
* Disable/relax a few tests failing in Android 2.3 ([#1785](https://github.com/jquery/jquery/issues/1785), [704de81](https://github.com/jquery/jquery/commit/704de8180f220afa1efd7bd65e9aeb9007a4f238))
* add the current version of node and iojs to the travis config ([dd2e027](https://github.com/jquery/jquery/commit/dd2e02715366d6959ae2c61c3e11fecb481374f4))
* Use QUnit URL parameter parsing ([fb98ea4](https://github.com/jquery/jquery/commit/fb98ea49b63ec444bb6f24c65b49a3e6cebcfc99))
* fix support values for android ([d224acb](https://github.com/jquery/jquery/commit/d224acbe47965397e3fe5bac569c4559e20aa997))
* Use standard external domain name ([3680689](https://github.com/jquery/jquery/commit/36806891657b0a3b7c4a12d9698f2ebf552fd712))
* Partially use new qunit interface ([#2540](https://github.com/jquery/jquery/issues/2540), [4543815](https://github.com/jquery/jquery/commit/4543815eeda0d7299e701311ca4ac38f23dbaf3a))
* Remove test/data/ua.txt ([#2398](https://github.com/jquery/jquery/issues/2398), [d8037c6](https://github.com/jquery/jquery/commit/d8037c6d5267569b56221148164b4df71f6ae612))
* Lower the checks rounding error ([1390d07](https://github.com/jquery/jquery/commit/1390d0736f6cff7a75ec0730967a98e26df1aa13))
* use assert syntax in restored test ([56b9656](https://github.com/jquery/jquery/commit/56b965655a293a6e1f09bf9c952d6175e6dba42b))
* don’t use deprecated argument in test declaration ([b8b111e](https://github.com/jquery/jquery/commit/b8b111e337e75010adf6bc610913f7e2084741bf))
* Tilt at a few style guide windmills ([4365133](https://github.com/jquery/jquery/commit/4365133defc4b78f4f55db932dd9b8c33f2b86b2))
* Make basic tests work in IE 8 ([f709a28](https://github.com/jquery/jquery/commit/f709a284e2ae343d9425a567a663ccd7adcd21d0))
* Remove Edge version from the user agent ([1d052bd](https://github.com/jquery/jquery/commit/1d052bdbe621ca111bab3314604dc682d900d716))
* Don’t load non-basic tests when basic module is selected ([06454d1](https://github.com/jquery/jquery/commit/06454d118f506baa351995c2a0337cba72ce5787))
* Minor updates for QUnit 1.16 compatibility ([f6f8848](https://github.com/jquery/jquery/commit/f6f8848fbe477fa93fd27ac7f10885dd6e97f633))
* Update QUnit ([b6e31a8](https://github.com/jquery/jquery/commit/b6e31a88332e70f7691b75afe187c7070e70e4fb))
* Fix merge conflict ([d07774a](https://github.com/jquery/jquery/commit/d07774ae0632a8a43ff490562c0e9bb3ae63e2dc))
* Backport basic tests from master ([#2505](https://github.com/jquery/jquery/issues/2505), [c7d458f](https://github.com/jquery/jquery/commit/c7d458fb9e86603ba43e3e7ee292e5655419dfa6))
* Keep test iframes around for assertions ([06128a9](https://github.com/jquery/jquery/commit/06128a9d7737310697ddeeacda3843bdf4793db3))
* Restore IE8 workarounds (Sinon timers for IE & HTML5 shiv) ([0b07c65](https://github.com/jquery/jquery/commit/0b07c652506c957e1de9eb8a620bc35f6c78296a))
* correct revert artefact ([b85f32f](https://github.com/jquery/jquery/commit/b85f32f74e54032c8347d5b045993615a9fabded))
* Add .extend test for defined accessor properties ([15f7920](https://github.com/jquery/jquery/commit/15f79201c40fda064d184392da33b88a727720da))
* further improvements QUnit 2.0 migration ([2f0cedc](https://github.com/jquery/jquery/commit/2f0cedc9972efa4bf9eb656001a098d9c51e53ec))
* Correct a typo in the regex matching Safari 8 ([ef332c7](https://github.com/jquery/jquery/commit/ef332c7c7b14533a078860e3e1527acfa59a26a7))
* more style corrections ([d8b7e7b](https://github.com/jquery/jquery/commit/d8b7e7b0bd047f02890de2874cafdd3e0f8dd608))
* Change quotes according to style guidelines ([52491ae](https://github.com/jquery/jquery/commit/52491ae3f0e2455b31686ec611546dc99e30d944))
* Fix CSS relative adjustment test for round-down browsers ([4a8000b](https://github.com/jquery/jquery/commit/4a8000b51a9854e21361e435e4c9b9cbd8ac458a))
* Add Microsoft Edge results (from Windows 10 build 10130) ([546593b](https://github.com/jquery/jquery/commit/546593bdd29752def705b172380b737ce8758ba9))
* fix tests in accordance with new :visible behavior ([cbd51c5](https://github.com/jquery/jquery/commit/cbd51c50b3b38574ba86093df34f88eaae5d294f))
* Accommodate page changes from the QUnit HTML reporter ([b747537](https://github.com/jquery/jquery/commit/b747537f9e26b35e43d785ec3b98a2cad3e4bf46))

#### Traversing

* Don’t expose jQuery.dir & jQuery.sibling ([#2512](https://github.com/jquery/jquery/issues/2512), [8c851bf](https://github.com/jquery/jquery/commit/8c851bfdb952f2aa0b71bf30194184f954af2215))

#### Wrap

* correct tests length ([f21d43a](https://github.com/jquery/jquery/commit/f21d43a1146256379d7f5b7cb537ed59aeebdeb4))


## 1.12.1 and 2.2.1

_2016-02-22_ - [blog post](https://blog.jquery.com/2016/02/22/jquery-1-12-1-and-2-2-1-released/)

* These two patch releases fix a few bugs and improve stability. The most significant bug fix involved a problem with the `.position()` method, which affected how jQuery UI tooltips were positioned in Internet Explorer.
* [修复] ……

## 1.12.2 and 2.2.2

_2016-03-17_ - [blog post](https://blog.jquery.com/2016/03/17/jquery-1-12-2-and-2-2-2-released/)

* These releases include a few bug fixes, which includes two edge case bugs for `jQuery.isPlainObject` and a bug when setting the selected property on an option element using the `.prop()` method in IE 11.
* [修复] ……

## 1.12.3 and 2.2.3

_2016-04-05_ - [blog post](https://blog.jquery.com/2016/04/05/jquery-1-12-3-and-2-2-3-released/)

* These are small releases with a couple bug fixes. There was a minor issue that made the 1.x branch inconsistent with 2.x and a recently-introduced bug in both branches that affected the `.load` method.
* [修复] ……
