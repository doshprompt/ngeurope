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

## Cordova

> Using Angular & Phonegap to build hybrid mobile applications

**Presenter(s):** Julien Bouquillon of Revolunet  
**Slides:** http://goo.gl/qA7l5u  
**Video:** http://youtu.be/yKjgbDEtCgM  
**Demo:** http://revolunet.github.io/angular-ngcordova-demo  
**Code:** https://github.com/revolunet/angular-ngcordova-demo  

- OpenSource part of PhoneGap
- Backed by Google, Adobe etc.
- Allows embedding of SPA in native browser
- Adds JS bridge for platform-specific APIs like file browser, GPS etc.
- Cordova CLI or Node.js module or scripting via hooks
- ng-cordova plugin system by Ionic to use only JS to call out to some APIs which may be mocked via DI for testing

## Material Design

> https://www.polymer-project.org/

**Presenter(s):** Thomas Burleson, Max Lynch  
**Slides:** http://goo.gl/Htbhuw  
**Video:** http://youtu.be/2qiyhkQVyxE  
**Demo:** https://material.angularjs.org/  

- [Polymer Component Developement](https://www.polymer-project.org/docs/start/tutorial/intro.html)
- [Material Design Paper Elements](http://www.google.com/design/spec/material-design/introduction.html)
- [Topeka SPA from Google I/O 2014](https://polymer-topeka.appspot.com/)

## Dgeni

> Documentation generation on steroids

**Presenter(s):** Pete Bacon Darwin  
**Slides:** http://goo.gl/6dISbg  
**Video:** http://youtu.be/PQNROxXajyQ  

- succeeds __*ngdocs*__
- built on top of _node.js_

## Protractor

> Testability API

**Presenters:** Julie Ralph, Chirayu Krishnappa  
**Slides:** http://goo.gl/yWqIzW  
**Video:** http://youtu.be/XgmUkCISabc  

- e2e testing - everything together to increase confidence in your code
- reputation for being flaky, hard to debug, painful
- user is actually typing vs. setting a value directly, requires all elements with interactions to be visible in context
- node module (written in JS) built on top of a tool called WebDriver (standard)
- protocol gives us methods for common use-cases
- separation of config from actual test logic
- relies on a Selenium Server running somewhere
- element() returns an elementFinder
- Goes over Command Queue (Control Flow)
- does promise chaining behind the scenes but can explicitly use .then() also
- Best Practice - limit logic in tests to not replicate production code, cover for loops etc.
- Page-Object Model (POM) - promotes element reuse and allows for changes to be made and effected universally
- debug with pause()
- Testability API - agnostic to version of angular, very basic but more tools to come soon
- findBindings, get/set location, turn off animations (don’t have to account for animation time so tests are fast, testing core functionality), getStable (notify when all pending async operations known to ng are completed, none are pending - expect() uses that so no need to use magic timeouts that may break, and instead automatically wait the exact amount of time, waiting is hidden from you so it’s as though you are writing synchronous tests)
- don’t want to write debugging code in production
  - sloppy - Testability is encapsulated in a service
  - insecure - client-side code is visible anyway
  - file size - minimal increase (<1KB)
  - slow - work deferred until it’s called, able to turn off and ptor will turn on when it needs to

## New Router

**Presenter(s):** Rob Eisenberg  
**Slides:** http://goo.gl/33Jlb6  
**Video:** http://youtu.be/h1P_Vh4gSQY  

- backport to 1.3
- New Features - Conventions, Navigation Model, Document Title Updates (hash, push changes)
- Dynamic Loading - ability to load controllers on the fly
- Child Apps - more than one router in a single app (app router + child router per controller, features managed by teams can own their own router(s), aka nested router or tree of child apps, tabs are completely encapsulated by mapped to the urls generated dynamically, state management and component reuse, parallel controllers)
- Screen Activation - move from one screen to another with unsaved data (lifecycle:- TO: canActivate > activate, FROM: canDeactivate > deactivate; handles promises for async calls to DB/api before resolving hooks, NavigationCommands - low level control of the router like a redirect if they don’t have rights or you can write your own to take control of the router midway)
- Navigation Pipeline (can pull out stuff or add more new custom steps like user permissions, validations)
- Customizations  - Configurations/Conventions, NavigationInstruction (per controller), NavigationContext, History, Viewport
- demo code - based on an old version of angular 2.0 templating and back port not finished yet

## angular-ui/bootstrap

> Lessons learned: improving flexibility

**Presenter(s):** Pawel Kozlowski  
**Slides:** http://goo.gl/3pmMup  
**Video:** http://youtu.be/tfVA1syv-3o  

- __*Philosophy*__ - lightweight, native directives with ONLY bootstrap CSS, flexible / customizable, tested
- don’t put markup in javascript, keep them separated (like ng manages templates for directives) so easy to change styling instead of forking and manually gripping and painstakingly changing it
- preload templates using __*$templateCache*__ since it’s just a unique id
- customizing functionality using settings/configuration - essential options vs any-and-all configurations
- __*Controller*__ - extension for your logic but if you dump it all in the linking function then nobody can access it, but if you provide in controller than people can access it, decorate it or modify it. Don’t want to get a PR for every possible scenario
- think of the controller as the point of extension instead of a bulky one-size-fits-all API
- __*Aggregation*__ - if multiple directives on angular target the same name, they are all run in order (stacking directives on top of one another) so build from smaller directives to combine them into one bigger powerful directive
- Sometimes directives are not the best abstraction - `<modal>` vs `$modal` 
- __*Takeaways*__ - don’t guess, enlarge APIs at your discretion only as and when use-cases emerge and are justified
- Examples
  - [Hacking Core Directives in AngularJS](http://briantford.com/blog/angular-hacking-core) blog post by Brian Ford
  - [Testing Angular Directives](https://github.com/vojtajina/ng-directive-testing) on GitHub by Vojta Jína
  - Draggable Modal live demo

## Angular from Scratch

> https://github.com/Swiip/angular-from-scratch

**Presenter(s):** Matthieu Lux

- simplified implementations — event loop, scope, watchers, digest, apply
- compiler - directives (ng-bind, ng-model)
