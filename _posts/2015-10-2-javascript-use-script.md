---
layout: post
title: JavaScript Use Strict
---

If you’re starting to encode javascript or you are already a javascript programmer and have never seen the strict mode before, check out this post.

![Javascript Use Strict]({{ site.url }}/images/posts/strict-mode.png)

## About strict mode

I always recommend coding javascript in strict mode. Strict mode makes changes to normal javascript semantics. An important aspect is that the strict mode eliminates silent errors, forcing you to write a better code and don’t make mistakes.

## Invoking strict mode

To invoke the strict mode, you just need to write ‘use strict'; in your javascript file, for example.

```javascript
'use strict';
```

Now that you already know how to invoke strict mode, let’s see a quick example.

## Quick example

```javascript
'use strict';
foo = 'Guilherme'; // ReferenceError
```

The error occurs because you need to declare the variable.

```javascript
'use strict';
var foo = 'Guilherme'; // It works!
```

Now it works!

## Conclusion

As you can see, strict mode can help you a lot to write a better javascript code. If you wanna see more examples and know more how it exactly works, take a look: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode