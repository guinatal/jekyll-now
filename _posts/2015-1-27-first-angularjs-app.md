---
layout: post
title: First AngularJS App
---

Hello! This is my first post and I have decided to write about AngularJS. I am still improving my skills with Angular and I would like to share my knowledge. Today, we are going to see how to start an AngularJS App and learn basic concepts like Module, Directives and Expressions.

![AngularJS]({{ site.url }}/images/posts/angularjs.png)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>First AngularJS App</title>
  </head>
  <body>
    <h1>First AngularJS App</h1>
  </body>
</html>
```

The first thing we need to do is to import the AngularJS library and initialize the application through the ng-app directive. After that, the app is ready to read Angular codes.

```html
<!DOCTYPE html>
<html ng-app> <!-- Directive -->
  <head>
    <title>First AngularJS App</title>
  </head>
  <body>
    <h1>First AngularJS App</h1>

    <!-- Expressions -->
    <p>8 + 5 = {{ 8 + 5 | angular }}</p>
    <p>100 / 2 = {{ 100 / 2 }}</p>
    <p>100 * 2 + 1 = {{ 100 * 2 + 1 }}</p>
    <p>Currency = {{ 100 | currency }}</p>

    <!-- AngularJS Library -->
    <script src="angular.min.js"></script>
  </body>
</html>
```

AngularJS extends HTML attributes with Directives, and binds data to HTML with Expressions. In the following link you have a list of directives https://docs.angularjs.org/api/ng#directive

### Controllers

AngularJS applications are controlled by controllers. The ng-controller directive defines the application controller.
First of all, we need to create an Angular Module for our application.

```html
<html ng-app="myApp">
```

It is time to build our application file. Let’s create the app.js file and import it. As you can see, the controller is attached (inside) to the application.

```html
<script src="app.js"></script>
```

```javascript
(function(){
  var myApp = angular.module('myApp', []);

  // Controller
  myApp.controller("myController", function(){

    this.user = obj;

  });

  var obj = {
    name: 'Guilherme',
    password: '123',
    age: '23'
  }

})();
```

In our current HTML, we have the directive (ng-controller), controller name (myController) and an Alias (controller).

```html
<!DOCTYPE html>
<html ng-app="myApp"> <!-- Directive -->
  <head>
    <title>First AngularJS App</title>
  </head>
  <body>
    <h1>First AngularJS App</h1>

    <!-- Expressions -->
    <article>
      <h1>Expressions</h1>
      <p>8 + 5 = `{{ 8 + 5 }}`</p>
      <p>100 / 2 = \{{ 100 / 2 }}</p>
      <p>100 * 2 + 1 = {{ 100 * 2 + 1 }}</p>
      <p>Currency = {{ 100 | currency }}</p>
    </article>

    <!-- Controller -->
    <article ng-controller="myController as controller">
      <h1>Controller</h1>
      <p>{{ controller.user.name }}</p>
      <p>{{ controller.user.password }}</p>
      <p>{{ controller.user.age }}</p>
    </article>

    <!-- AngularJS Library -->
    <script src="angular.min.js"></script>
    <!-- External Javascript -->
    <script src="app.js"></script>
  </body>
</html>
```

## Conclusion

We have just made a very simple app using AngularJS, but I believe that now you (if had never seen) have an idea of the power and simplicity of this great javascript framework. I did and recommend the free course of AngularJS. http://campus.codeschool.com/courses/shaping-up-with-angular-js