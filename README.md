# ez-scss

This is a library of mixin functions for [Scss/Sass](https://sass-lang.com/guide) to help minimise code and increase the readability of stylesheets.
Created by Daniel Scott, founder of [Life of Dan](https://life-of-dan.dev).

> If you have any requests for features please either open an issue in the [git repo](https://github.com/life-of-dan/ez-scss) or [email me](mailto:me@life-of-dan.dev)

## Getting Started

All you have to do is import the scss mixins you need file:

```scss
@import 'ez-scss/responsive'; // for responsive sizing
@import 'ez-scss/mixins'; // toolkit to shorten css props

// rest of your code...
```

Then include the mixins where ever you like!

```scss
@import 'ez-scss/responsive';

// BEFORE
@media (max-width: 425px) {
  font-size: 1rem;
  padding: 8px 16px;
  width: fit-content;
}

@media (max-width: 320px) {
  padding: 4px 8px;
}

// AFTER ~ improved readability
@include mobile-l {
  font-size: 1rem;
  padding: 4px 16px;
  width: fit-content;
}

@include mobile-s {
  padding: 4px 8px;
}
```

```scss
@import 'ez-scss/mixins';

// BEFORE
div {
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  flex-direction: column;
  flex-wrap: wrap;
  width: 100vw;
  height: 100vh;
}

// AFTER
div {
  @include setFlex(center, center, center, column, wrap);
  @include setSize(100vw, 100vh);
}
```

## Helpful Notes

I highly recommend installing a SCSS Intellisense library such as [SCSS Intellisense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss) by mrmlnc for VScode. This will show you a popup of parameter names as you type mixins in from the documentation.

## Overview

### Mixins

```scss
@include setSize(auto, auto); // $width, $height
```

```scss
@include setMarginPadding(auto, auto); // $margin, $padding
```

```scss
@include setPosition(
  static,
  auto,
  auto,
  auto,
  auto
); // $position, $top, $left, $bottom, $right
```

```scss
@include setDisplay(
  inline,
  static,
  auto,
  auto
); // $display, $position, $top, $left
```

```scss
@include setFlex(
  normal,
  normal,
  normal,
  row,
  nowrap
); // $justifyC, $alignI, $alignC, $flexDir, $flexWrap
```

```scss
// Absoultely centers selector the old fashion way, the ol block/transform ;)
@include absoluteCenter();
```

```scss
// Disables ability to select (highlight with mouse drag) text or image on element
@include disableSelect();
```

```scss
@include onHoverBoxShadow(
  1s,
  0px,
  -5px,
  0px,
  3px,
  rgb(0, 0, 0, 0.5)
); // $duration, $LRsides, $TBsides, $all, $blur
```

### Responsive

```scss
@include mobile-s {
  // 320px width or less specific content
}
```

```scss
@include mobile-m {
  // 375px width or less specific content
}
```

```scss
@include mobile-l {
  // 425px width or less specific content
}
```

```scss
@include tablet {
  // 768px width or less specific content
}
```

```scss
@include laptop {
  // 1024px width or less specific content
}
```

```scss
@include laptop-l {
  // 1440px width or less specific content
}
```

```scss
@include four-k {
  // 2560px width or less specific content
}
```
