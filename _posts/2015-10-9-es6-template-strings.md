---
layout: post
title: ES6 Template strings
---

Quick post about template strings. If you are learning Ecmascript 6, you should read this post. This is the new way to embed variables in texts.

![ES6 Template strings]({{ site.url }}/images/posts/template-strings.png)

## About

*Template strings are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them.* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/template_strings

Template strings are enclosed by the back-tick (` `). So if you don’t have been using the back-tick, you should find it now on your keyboard, it will be very used from now.

To embed a variable in a text, you need to indicate it by the Dollar sign and curly braces (${expression}).

## Examples

### Syntax

```javascript
'use strict';

let age = 23;

console.log('I am ' + age + ' years old.'); // normal strings

console.log(`I am ${age} years old.`); // template strings
```

### Multi-line strings

```javascript
'use strict';

// normal strings

console.log("my text line 1\n" + 
"my text line 2\n" + 
"my text line 3\n" + 
"my text line 4\n");

// template strings

console.log(`my text line 1
my text line 2
my text line 3
my text line 4`);
```

### Expressions

```javascript
'use strict';

let a = 13;
let b = 10;

// normal strings

console.log("I am " + (a + b) + " years old and not " + (2 * a + b) + ".");

// template strings

console.log(`I am ${a + b} years old and not ${2 * a + b}.`);
```

## Conclusion

Template strings are already being used and will be used more and more. So if you’re not used to it, get used to!
For you who is studying Ecmascript 6, take a look: https://github.com/airbnb/javascript (Airbnb JavaScript Style Guide)
