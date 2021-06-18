# WOW-RRO.js

基于 [wowjs](https://github.com/matthieua/WOW) 开发，增强适配 DOM 滚动情景

## Documentation

[wowjs documentation ➫](http://delac.io/WOW/docs.html)

### Dependencies

- [animate.css](https://github.com/daneden/animate.css)

### Basic usage

在需要设置动画的元素上设置可见性为 hidden

- CSS

```css
.wow {
  visibility: hidden;
}
```

- HTML

```html
<section class="wow slideInLeft"></section>
<section class="wow slideInRight"></section>
```

- JavaScript

```javascript
new WOW().init();
```

### Advanced usage

- HTML

```html
<section class="wow slideInLeft" data-wow-duration="2s" data-wow-delay="5s"></section>
<section class="wow slideInRight" data-wow-offset="10" data-wow-iteration="10"></section>
```

- JavaScript

```javascript
var wow = new WOW({
  parentClass: window, // 默认为window，可设置对应的DOM
  boxClass: 'wow', // animated element css class (default is wow)
  animateClass: 'animated', // animation css class (default is animated)
  offset: 0, // distance to the element when triggering the animation (default is 0)
  mobile: true, // trigger animations on mobile devices (default is true)
  live: true, // act on asynchronously loaded content (default is true)
  callback: function (box) {
    // the callback is fired every time an animation is started
    // the argument that is passed in is the DOM node being animated
  },
  scrollContainer: null, // optional scroll container selector, otherwise use window
});
wow.init();
```

### 兼容性

- IE 10+
- Firefox 14+
- Modern Browser
