---
layout: post
title: querySelector vs getElementById
---

I’ve realized that most of people usually don’t use the querySelector, thus I decided to write quick examples and the basic differences between querySelector and selectElementById as well as querySelectorAll and getElementsByClassName.

http://www.w3.org/TR/selectors-api/

“Selectors, which are widely used in CSS, are patterns that match against elements in a tree structure. The Selectors API specification defines methods for retrieving Element nodes from the DOM by matching against a group of selectors. It is often desirable to perform DOM operations on a specific set of elements in a document. These methods simplify the process of acquiring specific elements, especially compared with the more verbose techniques defined and used in the past.”

## querySelector vs selectElementById

Let’s assume the following code:

```html
<form id="userForm">
  <input id="username" type="text" value="Guilherme" />
</form>
```

We want to get the username element and allocate it in a variable. First let’s do this using getElementById.

```javascript
var username = document.getElementById("username");
```

Now, let’s get the same element but this time using querySelector.

```javascript
var username = document.querySelector("#userForm #username");
```

As you can see, using the querySelector the element that we want to select is much more specific and defined. The result is exactly the same.

![getElementById vs querySelector]({{ site.url }}/images/posts/getElementById-image-1.png)

## querySelectorAll vs selectElementByClassName

Let’s assume the following code:

```html
<form id="productForm">
  <input id="productOne" class="product" type="text" value="Product 1" />
  <input id="productTwo" class="product" type="text" value="Product 2" />
  <input id="productThree" class="product" type="text" value="Product 3" />
</form>
```

We want to get all the products elements and allocate them in a variable. First let’s do this using getElementByClassName.

```javascript
var products = document.getElementsByClassName("product");
```

Now, let’s get the same elements but this time using querySelectorAll.

```javascript
var products = document.querySelectorAll("#productForm .product");
```

The result is almost the same, but the getElementsByClassName returns a HTMLCollection and the querySelectorAll returns a NodeList.

![getElementsByClassName vs querySelectorAll]({{ site.url }}/images/posts/getElementById-image-2.png)

Great! But these examples are very simple, so let’s try something a bit more difficult.

```html
<table id="tableProducts">
  <thead>
    <tr>
      <th>Product</th>
      <th>Value</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>A</td>
      <td>100</td>
    </tr>
    <tr>
      <td>B</td>
      <td>200</td>
    </tr>
    <tr>
      <td>C</td>
      <td>300</td>
    </tr>
  </tbody>
</table>
```

In the example above, we have a table of products and we need to sum the values. I guess that there are some ways to do it, but let’s use querySelectorAll.

```javascript
var sum = 0;
var cells = document.querySelectorAll("#tableProducts>tbody>tr>td:nth-of-type(2)");

for (var i = 0; i < cells.length; i++)
  sum += parseFloat(cells[i].firstChild.data);
```

Very simple, isn’t it?

## Conclusion

The querySelector and querySelectorAll are really very powerful and work well when you need to select more specific elements. They are supported by most of current browsers. If you wish, here you can check the supported browsers: https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector#Browser_Compatibility