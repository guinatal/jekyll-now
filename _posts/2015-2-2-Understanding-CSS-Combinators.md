---
layout: post
title: Understanding CSS Combinators
---

Have you already used the following combinator before?

```css
div ~ p {
  background-color: skyblue;
}
```

We have just seen the general sibling selector and it can be very useful. Let’s check it out! There are four combinators in CSS3.

- Descendant Selector
- Child Selector
- Adjacent Sibling Selector
- General Sibling Selector CSS3

![Combinators]({{ site.url }}/images/posts/Combinators.png)

### Descendant Selector

The descendant selector matches all elements that are descendants of a specified element. The following example selects all p elements inside div elements:

```css
div p {
  background-color: skyblue;
}
```

```html
<article>
  <h1>Descendant Selector</h1>
  <div>
    <p>Descendant Selector 1</p>
    <p>Descendant Selector 2</p>
    <section>
      <p>Descendant Selector 3</p>
      <p>Descendant Selector 4</p>
    </section>
  </div>
  <p>Descendant Selector 5</p>
  <p>Descendant Selector 6</p>
</article>
```

![Descendant Selector]({{ site.url }}/images/posts/Descendant-Selector.png)

### Child Selector

The child selector selects all elements that are the immediate children of a specified element. The following example selects all p elements that are immediate children of a div element:

```css
div > p {
  background-color: skyblue;
}
```

```html
<article>
  <h1>Child Selector</h1>
  <div>
    <p>Child Selector 1</p>
    <p>Child Selector 2</p>
    <section>
      <p>Child Selector 3</p>
      <p>Child Selector 4</p>
    </section>
  </div>
  <p>Child Selector 5</p>
  <p>Child Selector 6</p>
</article>
```

![Child Selector]({{ site.url }}/images/posts/Child-Selector.png)

### Adjacent Sibling Selector

The adjacent sibling selector selects all elements that are the adjacent siblings of a specified element. Sibling elements must have the same parent element, and “adjacent” means “immediately following”. The following example selects all p elements that are placed immediately after div elements:

```css
div + p {
  background-color: skyblue;
}
```

```html
<article>
  <h1>Adjacent Sibling Selector</h1>
  <div>
    <p>Adjacent Sibling Selector 1</p>
    <p>Adjacent Sibling Selector 2</p>
    <section>
      <p>Adjacent Sibling Selector 3</p>
      <p>Adjacent Sibling Selector 4</p>
    </section>
  </div>
  <p>Adjacent Sibling Selector 5</p>
  <p>Adjacent Sibling Selector 6</p>
</article>
```

![Adjacent Sibling Selector]({{ site.url }}/images/posts/Adjacent-Sibling-Selector.png)

### General Sibling Selector

The general sibling selector selects all elements that are siblings of a specified element. The following example selects all p elements that are siblings of div elements:

```css
div ~ p {
  background-color: skyblue;
}
```

```html
<article>
  <h1>General Sibling Selector</h1>
  <div>
    <p>General Sibling Selector 1</p>
    <p>General Sibling Selector 2</p>
    <section>
      <p>General Sibling Selector 3</p>
      <p>General Sibling Selector 4</p>
    </section>
  </div>
  <p>General Sibling Selector 5</p>
  <p>General Sibling Selector 6</p>
</article>
```

![General Sibling Selector]({{ site.url }}/images/posts/General-Sibling-Selector.png)

### Conclusion

If you are a new learner or just improving your CSS skills, you need to know that CSS Combinators are used all the time by front-end developers. We have just seen very basic examples and most of the times they are used just like that. But you can also make different combinations using all of them.