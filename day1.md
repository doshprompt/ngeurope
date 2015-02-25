![ngEurope 2014](https://raw.githubusercontent.com/doshprompt/ngeurope/master/ng-europe-horizontal-on-black.png)

---

## Keynote

> State of Angular

**Presenter(s):** Igor Minar, Brad Green  
**Slides:** http://goo.gl/70sEsr  
**Video:** http://youtu.be/c5HSqDLfpW0  

- Material Design (angular-material) library baked in for basic responsive, mobile
- ngAria for screen readers, accessible to all on mobile also
- Angular 2.0 push (ES6 + types ++)
- Perf + Mobile + Developer friendly (scaleable, IDE support for template linting etc.)
- Educators
	- [JohnLindquist](egghead.io)
    - [Dan Wahlin](weblogs.asp.net/dwahlin)
	- [codeschool.com](http://www.codeschool.com)
	- [pluralsight.com](http://www.pluralsight.com)
	- [thinkster.io](http://thinkster.io)
- Style Guides
	- [Google’s AngularJS style guide](http://google-styleguide.googlecode.com/svn/trunk/angularjs-google-style.html)
	- [John Papa’s style guide](https://github.com/johnpapa/angularjs-styleguide)
	- [Todd Motto’s style guide](https://github.com/toddmotto/angularjs-styleguide)

## Angular 1.3

> http://petermorlion.blogspot.com/2014/10/ngeurope-whats-new-in-angular-13.html

**Presenter(s):** Jeff Cross, Brian Ford  
**Slides:** http://goo.gl/pNmhAa  
**Video:** http://youtu.be/ojMy6m_fcxc  

- Free performance improvements (debugMode, applyAsync, bindOnce i.e. ::prefix)
- SVG namespace custom directives now work well, don't throw errors
- ngMessages make code more DRY, no more ng-show / ng-hide / ng-if bombarding users with errors
- ng-model-options like debounce, updateOn 'blur' etc. supported natively
- validators, async validators
- $watchGroup takes array of $scope props to watch
- ngAria for base level accessibility
- ng-strict-di + ng-annotate instead of ngmin
- allOrNothing to prevent making invalid http requests

## Ionic Framework

**Presenter(s):** Andrew Joslin  
**Slides:** N/A  
**Video:** http://youtu.be/ZjPRj2Vp74U  

- material design for Android coming soon
- no planned full tablet support
- no desktop support due to scrolling, animations weirdness
- Ionic Creator with drag-and-drop components
- Ionic Snapshot to compare releases by taking screenshots and using image processing algos

## AngularDart

> Under the hood

**Presenter(s):** Victor Berchet, Rado Kirov  
**Slides:** http://goo.gl/ADjgcg  
**Video**: http://youtu.be/RifbDsbfpYA  

- Used for some new ideas coming in AngularJS 2.0
- also uses DI
- HTML —> ViewFactory (compiled into ElementBinders)
- Uses WebComponents (@Component) like Directives thru ComponentFactory
- Complete Rendering Pipeline (chain fully explained step-by-step)
- Need to use @Decorator to mimic some angular directive behavior by recreating directive code in Dart’s decorator syntax (e.g. ngClick)
- Zones + Event Loop + Executor (VmTurnZone)

## Architecture

> Can we learn from architects?

**Presenter(s):** Vojta Jína  
**Slides:** http://goo.gl/u27Otl  
**Video:** http://youtu.be/mqlYLbB9O3g  
**Additional Notes:** http://goo.gl/L4stz1  

- Angular CI Server (on Travis) is not stable - build broken doesn’t necessarily mean code is broken but rather test environment is unreliable
- Most code we write is crap, not maintainable
- Writing code is like making buildings
- Lots of math involved in architecture
- Principles can be related to writing software (order matters, pure functions with no side effects promotes caching, immutability, since mutation is once again affected by order of code execution)
- Caching may be expensive, dirty checking altos might be more work than just calling function no matter what, unless you are being careful with shared mutable states
- Simple examples for formulas for writing more predictable programming
