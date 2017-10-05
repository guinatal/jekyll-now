---
layout: post
title: Getting Started with Sass
---

Today I am going to talk about Sass and SCSS but there are others preprocessors available. For example: LESS.

Sass is a preprocessor that is interpreted into CSS. In practice it means you will write codes in Sass language and it will be converted into CSS. It helps you reduce repetition with your CSS.

![Getting Started with Sass]({{ site.url }}/images/posts/sass.png)

## Sass vs SCSS

Differences between Sass and SCSS. http://sass-lang.com/documentation/

Sass has two syntaxes. The most commonly used syntax is known as “SCSS” (for “Sassy CSS”), and is a superset of CSS3’s syntax. This means that every valid CSS3 stylesheet is valid SCSS as well. SCSS files use the extension .scss.

The second, older syntax is known as the indented syntax (or just “.sass”). Inspired by Haml’s terseness, it’s intended for people who prefer conciseness over similarity to CSS. Instead of brackets and semicolons, it uses the indentation of lines to specify blocks. Files in the indented syntax use the extension .sass.

## Getting Started

I considered writing about how to install the Sass but everything you need you can find here: http://sass-lang.com/install

### Finally, let’s write some code!

The first thing you need to know is that Sass allows you to use variables. It keeps your code much more organized.

SASS SYNTAX

```sass
$font-stack: Helvetica, sans-serif
$primary-color: #333
$font-small: 15px
$font-medium: 30px
$font-large: 60px
$blue: #186DEE
$grey: #E5E5E5
```

SCSS SYNTAX

```scss
$font-stack: Helvetica, sans-serif;
$primary-color: #333;
$font-small: 15px;
$font-medium: 30px;
$font-large: 60px;
$blue: #186DEE;
$grey: #E5E5E5;
```

The second thing you need to know is that with Sass your code will be much more organized visually as well. Sass and SCSS are written in a visual hierarchy.

SASS SINTAX

```scss
.content
  padding: 20px
  background-color: $grey
  +border-radius(5px)

  &:hover
    background-color: $blue

  span
    display: block

  span.one
    font-size: $font-small

  span.two
    font-size: $font-medium

  span.three
    font-size: $font-large
```

SCSS SINTAX

```scss
.content {
  padding: 20px;
  background-color: $grey;
  @include border-radius(5px);

  &:hover {
    background-color: $blue;
  }

  span {
    display: block;
  }

  span.one {
    font-size: $font-small;
  }

  span.two {
    font-size: $font-medium;
  }

  span.three {
    font-size: $font-large;
  }
}
```

Note: in the code below we are using a mixin. But to use it, we need to create it. Otherwise our code will not compile.

## Mixins

*A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. You can even pass in values to make your mixin more flexible.* http://sass-lang.com/guide

SASS SINTAX

```sass
=border-radius($radius)
  -webkit-border-radius: $radius
  -moz-border-radius: $radius
  -ms-border-radius: $radius
  border-radius: $radius
```

SCSS SINTAX

```scss
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
  -moz-border-radius: $radius;
  -ms-border-radius: $radius;
  border-radius: $radius;
}
```

## Conclusion

Writing codes in Sass or SCSS is really very simple and even if you have never seen them before, but you have a good knowledge of CSS, you will able to assimilate, understand and write codes.

If you want to practise and improve your skills, there are some online compilers and you can use them for free. Take a look at http://sassmeister.com/

There’s another good service if you don’t want to write your own mixins: here you can find a simple and lightweight mixin library for Sass. http://bourbon.io/