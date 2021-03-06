# Material Design for Angular 2
[![npm version](https://badge.fury.io/js/%40angular%2Fmaterial.svg)](https://www.npmjs.com/package/%40angular%2Fmaterial)
[![Build Status](https://travis-ci.org/angular/material2.svg?branch=master)](https://travis-ci.org/angular/material2)
[![Gitter](https://badges.gitter.im/angular/material2.svg)](https://gitter.im/angular/material2?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

这是Angular团队在Angular 2之上构建的Material Design组件的家。

#### 快速链接
[Google group](https://groups.google.com/forum/#!forum/angular-material2),
[Contributing](./CONTRIBUTING.md),
[Plunker Template](http://plnkr.co/edit/o077B6uEiiIgkC0S06dd?p=preview)

### 入门

请参阅我们的[入门指南](./GETTING_STARTED.md),  
如果你正在使用Angular Material 2构建第一个项目。

### 项目状态
Angular Material 2 is currently in alpha and under active development. 
During alpha, breaking API and behavior changes will be occurring regularly.

Check out our [directory of design documents](https://github.com/angular/material2/wiki/Design-doc-directory) 
for more insight into our process.

If you'd like to contribute, you must follow our [contributing guidelines](./CONTRIBUTING.md). 
You can look through the issues (which should be up-to-date on who is working on which features 
and which pieces are blocked) and make a comment. 
Also see our [`Good for community contribution`](https://github.com/angular/material2/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+for+community+contribution%22) 
label.

High level items planned for November 2016:
* Initial version of md-select
* Continued bug bashing
* Initial versions of autocomplete and chips
* AoT compile e2e app
* Continue work on https://material.angular.io site
* Major refactoring for md-input
* Tabs animations
* Expanding e2e test coverage


#### 特征状态：

| Feature          | Status                              | Docs         | Issue          |
|------------------|-------------------------------------|--------------|----------------|
| button           |                           Available | [README][1]  |              - |
| cards            |                           Available | [README][2]  |              - |
| checkbox         |                           Available | [README][3]  |              - |
| radio            |                           Available | [README][4]  |              - |
| input            |                           Available | [README][5]  |              - |
| sidenav          |                           Available | [README][6]  |              - |
| toolbar          |                           Available | [README][7]  |              - |
| list             |                           Available | [README][8]  |   [#107][0107] |
| grid-list        |                           Available | [README][9]  |              - |
| icon             |                           Available | [README][10] |              - |
| progress-circle  |                           Available | [README][11] |              - |
| progress-bar     |                           Available | [README][12] |              - |
| tabs             |                           Available | [README][13] |              - |
| slide-toggle     |                           Available | [README][14] |              - |
| button-toggle    |                           Available | [README][15] |              - |
| slider           |                           Available | [README][16] |              - |
| menu             | Initial version, needs enhancements | [README][17] |   [#119][0119] |
| tooltip          | Initial version, needs enhancements | [README][18] |              - |
| ripples          |  Available, but needs to be applied | [README][19] |   [#108][0108] |
| dialog           |  Started, not yet ready for release | [README][22] |   [#114][0114] |
| snackbar / toast | Initial version, needs enhancements | [README][21] |   [#115][0115] |
| select           |                      Design started |           -  |   [#118][0118] |
| textarea         |                             Started |           -  |   [#546][0546] |
| autocomplete     |                      Design started |           -  |   [#117][0117] |
| chips            |                      Design started |           -  |   [#120][0120] |
| theming          | Initial version, needs enhancements | [Guide][20]  |              - |
| prod build       |                         Not started |           -  |              - |
| docs site        |   UX design and tooling in progress |           -  |              - |
| typography       |                         Not started |           -  |   [#205][0205] |
| layout           |      Design in-progress, prototyped |           -  |              - |
| fab speed-dial   |                         Not started |           -  |   [#860][0860] |
| fab toolbar      |                         Not started |           -  |              - |
| bottom-sheet     |                         Not started |           -  |              - |
| bottom-nav       |                         Not started |           -  |   [#408][0408] |
| virtual-repeat   |                         Not started |           -  |   [#823][0823] |
| datepicker       |                         Not started |           -  |   [#675][0675] |
| data-table       |                         Not started |           -  |   [#581][0581] |
| stepper          |                         Not started |           -  |   [#508][0508] |

 [1]: ./src/lib/button/README.md
 [2]: ./src/lib/card/README.md
 [3]: ./src/lib/checkbox/README.md
 [4]: ./src/lib/radio/README.md
 [5]: ./src/lib/input/README.md
 [6]: ./src/lib/sidenav/README.md
 [7]: ./src/lib/toolbar/README.md
 [8]: ./src/lib/list/README.md
 [9]: ./src/lib/grid-list/README.md
[10]: ./src/lib/icon/README.md
[11]: ./src/lib/progress-circle/README.md
[12]: ./src/lib/progress-bar/README.md
[13]: ./src/lib/tabs/README.md
[14]: ./src/lib/slide-toggle/README.md
[15]: ./src/lib/button-toggle/README.md
[16]: ./src/lib/slider/README.md
[17]: ./src/lib/menu/README.md
[18]: ./src/lib/tooltip/README.md
[19]: ./src/lib/core/ripple/README.md
[20]: ./docs/theming.md
[21]: ./src/lib/snack-bar/README.md
[22]: ./src/lib/dialog/README.md


[0107]: https://github.com/angular/material2/issues/107
[0119]: https://github.com/angular/material2/issues/119
[0108]: https://github.com/angular/material2/issues/108
[0114]: https://github.com/angular/material2/issues/114
[0115]: https://github.com/angular/material2/issues/115
[0118]: https://github.com/angular/material2/issues/118
[0546]: https://github.com/angular/material2/issues/546
[0117]: https://github.com/angular/material2/issues/117
[0120]: https://github.com/angular/material2/issues/120
[0123]: https://github.com/angular/material2/issues/123
[0205]: https://github.com/angular/material2/issues/205
[0860]: https://github.com/angular/material2/issues/860
[0408]: https://github.com/angular/material2/issues/408
[0508]: https://github.com/angular/material2/issues/508
[0823]: https://github.com/angular/material2/issues/823
[0675]: https://github.com/angular/material2/issues/675
[0581]: https://github.com/angular/material2/issues/581


"Available" means that the components or feature is published and available for use, but may still
be missing some behaviors or polish.

## Angular Material 目标
我们的目标是使用Angular 2和TypeScript构建一组高质量的UI组件，遵循Material Design规范。  
这些组件将作为如何按照最佳实践编写Angular代码的示例。

### 我们"高质量"的意思是什么?
* Internationalized and accessible so that all users can use them.
* Straightforward APIs that don't confuse developers.
* Behave as expected across a wide variety of use-cases without bugs.
* Behavior is well-tested with both unit and integration tests.
* Customizable within the bounds of the Material Design specification.
* Performance cost is minimized.
* Code is clean and well-documented to serve as an example for Angular devs.

## 浏览器和屏幕阅读器支持
Angular Material supports the most recent two versions of all major browsers: 
Chrome (including Android), Firefox, Safari (including iOS), and IE11 / Edge

We also aim for great user experience with the following screen readers:
* NVDA and JAWS with IE / FF / Chrome (on Windows).
* VoiceOver with Safari on iOS and Safari / Chrome on OSX.
* TalkBack with Chrome on Android.
