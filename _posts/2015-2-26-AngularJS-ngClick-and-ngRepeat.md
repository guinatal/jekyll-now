---
layout: post
title: AngularJS ngClick and ngRepeat
---

Second article about AngularJS and today we are going to see ngClick and ngRepeat directives. I’ve decided to write about these directives because they are very important and we use them all the time.

![AngularJS ngClick and ngRepeat]({{ site.url }}/images/posts/ngclick.png)

Let’s assume the following code

```javascript
(function(){

  var myApp = angular.module('myApp', []);

  myApp.controller("myController", function($scope){

  });

})();
```

Wrapping your Javascript in a closure is a good habit!

```html
<!DOCTYPE html>
<html ng-app="myApp">
  <head>
    <title>AngularJS ngClick and ngRepeat</title>
  </head>
  <body ng-controller="myController">

    <!-- ngClick example goes here -->

    <!-- ngRepeat example goes here -->

    <script src="angular.min.js"></script>
    <script src="app.js"></script>
  </body>
</html>
```

## ngClick

The first thing we need to do is to create a button in our HTML code and through the ngClick directive call the click function. After that, we will define the click function inside the controller.

```html
<button ng-click="click();">Click</button>

{{ message }}
```

```javascript
myApp.controller("myController", function($scope){

  $scope.click = function(){

    $scope.message = "It's working!";

  }

}
```

Great. The button is working through the ngClick directive and the message expression we’ve created was replaced by “It’s working”.

## ngRepeat

When we work with AngularJS, objects and arrays are used daily. Let’s continue our example including an array of objects and store the data inside the controller

```javascript
myApp.controller("myController", function($scope){
  
  $scope.message = "It's working!";
  $scope.users = json; // Storing data inside the controller

});

var json = [
  {name: "Guilherme", email: "guilherme@test.com", age: "22"},
  {name: "Milena", email: "milena@test.com", age: "26"}
];
```

Now we’ve got a user array, simulating a JSON in the real life ;) How do we print out this data inside our webpage? We need to use the ngRepeat directive.

```html
<ul>
  <li ng-repeat="user in users">{{ user.name }}</li>
</ul>
```

The page has been printed out with all the names. But we need to print out the email as well as the age. What do you think about changing the list to a table? It will be easy.

```html
<table>
  <tr ng-repeat="user in users">
    <td>{{ user.name }}</td>
    <td>{{ user.email }}</td>
    <td>{{ user.age }}</td>
  </tr>
</table>
```

What if we want to keep our list and print out the name, email and age?

```html
<ul>
  <li ng-repeat-start="user in users">{{ user.name }}</li>
  <li>{{ user.age }}</li>
  <li ng-repeat-end>{{ user.email }}</li>
</ul>
```

## Conclusion

The ngClick and ngRepeat directives are extremely easy to work with. JSON works great with the ngRepeat directive and it’s very common to use. You can find these examples on GitHub https://github.com/guinatal/blog-examples