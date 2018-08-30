# CSS

## Table of contents

* [Learning resources](#learning-resources)
* [Basics you need to know](#basics-you-need-to-know)
  * [Box Model setup](#box-model-setup)
  * [Global font reset and rem values](#global-font-reset-and-rem-values)
  * [Essential concepts](#essential-concepts)
    * [Box Model](#box-model)
    * [Properties](#properties)
    * [Positioning](#positioning)
  * [Typical structure of main CSS document](#typical-structure-of-main-css-document)
* [CSS Frameworks](#css-frameworks)
  * [Pure](#pure)
    * [Use Pure](#use-pure)
    * [Learn Pure](#learn-pure)

  

## Learning resources

1 **W3Schools**: https://www.w3schools.com/css/default.asp


## Basics you need to know

In this section you will find a list of things you should learn and know. This document doesn't explain things in detail, it only lists them. To learn in detail about CSS, use the W3Schools website.

### Box Model setup

A good way to set up a developer-friendly Box Model is a global setting of certain properties.  
`*` CSS rule means `for every HTML tag`.  

Make sure the below code is always positioned at the top of your main `.css` file.  

```
*, *:before, *:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0;
}
```

Read more: [CSS Tricks. Box-sizing](https://css-tricks.com/box-sizing/)

### Global font reset and rem values

Do not use `px` in any but `@media` rules, as they do not scale well with different devices (smartphones, etc.).  
Instead, always use `rem` values.  

In order to have properly scaled `rem` values, we need to use a reset trick. Make sure the below code is at the top of your main `.css` file, preceeded only by [Box-Model rule](#box-model).

```
html { 
  font-size: 62.5%; 
}
```

From now on, you should use `rem` values like so:  

```
.my-class {
  font-size: 1.6rem;
  width: 30rem;
}
```

With `font-size: 62.5%` property set on `html`, `0.1rem` now equals `1px`.  
Meaning (give the above example), `1.6rem` is equivalent to `16px`, and `30rem` to `300px`.  


### Essential concepts

#### Box Model 
Box Model (content, padding, border, margin)

#### Properties
  * sizes: `width`, `height`
  * boxes: `padding`, `padding-left`, `padding-right`, `padding-top`, `padding-bottom`, `margin`, `margin-left`, `margin-right`, `margin-top`, `margin-bottom`, `border`, `border-style`, `border-width`, `border-color`, `border-radius`
  * colours: `background`, `background-color`, `color`
  * text: `text-align`, `text-transform`, `font`, `font-size`, `font-weight`, `font-style`, `line-height`, `font-family`, `letter-spacing`, `word-spacing`
  * links: `text-decoration`
  * lists: `list-style-type`
  * images: `vertical-align`
  * shadows: `box-shadow`, `text-shadow`
  * pseudo classes: `:hover`, `:visited`, `:active`
  * positioning: `display`, `float`, `clear`
  * showing/hiding: `display`, `visibility`
  
#### Positioning
  * Float-ing (`float` & `clear`)
  * Inline-block (`display`)
  
  
### Typical structure of main CSS document

Feel free to use it as a template.  

```
*, *:before, *:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0;
}

html { 
  font-size: 62.5%; 
}

#wrapper {
  width: 100%;
}

img {
  max-width: 100%;
  vertical-align: middle;
}
```

Read more about `vertical-align`: https://css-tricks.com/what-is-vertical-align/

## CSS Frameworks

CSS Frameworks are sets of CSS rules (mostly classes) created to speed up developer's work.  
The two most popular CSS Frameworks:  
* [Bootstrap](https://getbootstrap.com/)
* [Foundation](http://foundation.zurb.com/)

Both are extremely comprehensive, but come at a price: they are quite big (file size-wise). What we aim at is Sustainable Web Design (more in [Sustainable Web Design tutorial](https://github.com/mkubera/bc_computing_stash/blob/master/tutorials/sustainable_web_design.md)), so we want to use a lightweight CSS Framework. Namely: [Pure.css](https://purecss.io/).

### Pure

Pure is a very small CSS Framework, weighing about 4kb. It is also modular (composed of modules, or `.css` files), so we can pick up just the modules we need, and make our environmental footprint even smaller. For example, if we only wanted to use two components (`Base` and `Grids`), we would only use 1.8kb.  

#### Use Pure

Most basic usage is to copy/paste the code below into the `<head>` section of your `.html` file.  

```
<link rel="stylesheet" 
      href="https://unpkg.com/purecss@1.0.0/build/pure-min.css" 
      integrity="sha384-nn4HPE8lTHyVtfCBi5yW9d20FjT8BJwUXyWZT9InLYax14RDjBj46LmSztkmNP9w" 
      crossorigin="anonymous">
```

##### Learn Pure

Pure comes with a very intuitive introduction and documentation.  

Learn Pure: [Pure.css](https://purecss.io/)
