---
layout: post
title: Javascript Hoisting
---

In the previous post, I wrote about strict mode in Javascript and how it is beneficial and helps you to write a better code. For example, to do not forget to declare a variable.

But, did you know that in Javascript you can declare a variable after accessing it?

![Javascript Hoisting]({{ site.url }}/images/posts/hoisting.png)

## Hoisting

In JavaScript, functions and variables are hoisted. Hoisting is JavaScript’s behavior of moving declarations to the top of a scope (the global scope or the current function scope). https://developer.mozilla.org/en-US/docs/Glossary/Hoisting

## Examples

### Variable

```javascript
'use strict';

x = 'Declaring a variable after using it.'; // It works!
document.write(x);

var x;
```

### Function

```javascript
myFunction(10); // It works!

function myFunction(x) {
    console.log(x);
}
```

Cool. You’ve just seen that you can declare variables and functions after accessing them.

## Ecmascript 6

Everybody is talking about Ecmascript 6, right? What about changing the example above from var to let and also make an example with class? It should work, right? Let’s see!

### let

```javascript
'use strict';

x = 'Declaring a variable after using it.'; // ReferenceError
document.write(x);

let x;
```

As you can see, let does not hoist the variable to the top of the block. You need to declare before using it.

### class

```javascript
var a = new myClass(1, 2); // ReferenceError

class myClass {
    constructor(x, y){
        this.x = x;
        this.y = y;
    }
}
```

Class declarations are not hoisted too. You first need to declare and then access it, otherwise code will throw a ReferenceError.

## Conclusion

Hoisting is an unknown or overlooked behavior of JavaScript (to many developers). All you need to do to avoid bugs is always declare all variables at the beginning of every scope. Of course, always using the javascript strict mode. If you didn’t see my post about strict mode, check it out: http://blog.guinatal.com/javascript-use-strict/