This is a library of mixin functions for [Scss](https://sass-lang.com/) to help minimise code and increase the readability of stylesheets.
Created by Daniel Scott, founder of [Daniels Designs](https://danielsdesigns.tech/).

## Getting Started

All you have to do is import the Scss file:

```scss
@charset "utf-8";
@import "../node_modules/ez-scss/mixins"; 

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