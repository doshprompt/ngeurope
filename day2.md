![ngEurope 2014](https://raw.githubusercontent.com/doshprompt/ngeurope/master/ng-europe-horizontal-on-black.png)

## Keynote

> AtScript

**Presenter(s):** Miško Hevery  
**Slides:** http://goo.gl/pwk6Pb  
**Video:** http://youtu.be/lGdnh8QSPPk  

- **NOT** building a language
- _"Sorry about Angular API"_, will fix it and make it better
- Why not building a language - already existing infrastructure, tooling, IDE support etc. and will make a new set of mistakes that you are not even aware of while fixing current mistakes, competing standards xkcd comic
- AtScript will ship with optional type system - RTTS Asserts
- Checking types at runtime - check the server’s JSON response for correct type(s)
- AtScript > TypeScript > ES6 > ES5

## Tooling

> Batarang

**Presenter(s):** Brian Ford  
**Slides:** http://goo.gl/Jb8V46  
**Video:** http://youtu.be/x8IWsjoCy-M  

- Vague definition: Thing that you go to when you don’t know what to do
- Documentation: under-utilized (tempted to say RTFM)
- I expected something to happen but nothing did (could be a typo, not sure where the error is — controller, directive, template etc.)
- I was doing it wrong because I didn’t know any better (where you manipulate the DOM, not sure where to put it)
- Hooks into Angular’s DI system
  - directives that don’t exist (typos)
  - unused modules (script(s) included but never injected where needed/used)
  - deprecated APIs (global controllers, ng-bind-html-unsafe removed)
  - enforce naming conventions (namespacing prefixes)
  - [Decorators](http://briantford.com/blog/angular-hacking-core)
- CI - automated code review
- Roadmap
  - performance hints (expensive watchers etc for smaller datasets before it goes into production with full datasets)
  - migration guide / codepath
  - hints integrate with text editor / IDE
