---
layout: post
title: CSS Fade In Animation
---

Have you already used a css animation in your project? They can make your website looks much more refreshed and modern visually. Today we’re gonna create the fadeIn effect.

![CSS Fade In Animation]({{ site.url }}/images/posts/fadeIn.png)

Let’s assume the following code:

```html
<h1>Hello World</h1>
<div class="circle"></div>
```
In the code above, if you click on the Result tab, you will see that the page loads at once, without any effect. We want to create an effect that when the page is loaded, the element loads in a fade effect.

## @keyframes and animation

First of all, we need to create our @keyframes from opacity 0 to 1.

```css
@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
```

Great, now we can create a class called fade-in and invoke our effect named fadeIn.

```css
.fade-in {
  opacity: 0; // invisible from the start
  animation: fadeIn ease-in 1; // call our keyframe named fadeIn, use animation ease-in and repeat it only 1 time
  animation-fill-mode: forwards; // this makes sure that after animation is done we remain at the last keyframe value (opacity: 1)
  animation-duration: 1s;
  animation-delay: 0.3s; // delay to start
}
```

Now, you just need to put the class fade-in in the element that you want to create the effect. If you want to create this effect for all your content, you can apply it on the body tag.

To see the final result, click on the Result tab below. You could also take a look on the CSS tab, I added some codes for better compatibility.

```css
<h1>Hello World</h1>
<div class="circle fade-in"></div>
```

## Conclusion

These effects are very simple to implement and make your website looks modern and even in some cases faster. If you want to learn more about CSS animation, I would recommend https://developer.mozilla.org/en-US/docs/Web/CSS/animation