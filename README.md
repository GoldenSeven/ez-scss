This is a library of mixin functions for [Scss](https://sass-lang.com/guide) to help minimise code and increase the readability of stylesheets.
Created by Daniel Scott, founder of [Daniels Designs](https://danielsdesigns.tech/).

## Getting Started

All you have to do is import the Scss file:

```scss
@charset "utf-8";
@import "DIR_OF_PROJECT/node_modules/ez-scss/mixins";

// rest of your code...
```

Then include the mixins where ever you like!

```scss
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

## Mixins

```scss

@include setSize(auto, auto); //$width, $height
```

```scss
@include setMarginPadding(auto, auto); // $margin, $padding
```

```scss
@include setPosition( static, auto, auto, auto, auto); // $position, $top, $left, $bottom, $right
```

```scss
@include setDisplay(inline,static,auto,auto); // $display, $position, $top, $left
```

```scss
@include setFlex(normal, normal, normal, row, nowrap); // $justifyC, $alignI, $alignC, $flexDir, $flexWrap
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
@include onHoverBoxShadow(1s, 0px, -5px, 0px, 3px, rgb(0, 0, 0, 0.5)); // $duration, $LRsides, $TBsides, $all, $blur
```
