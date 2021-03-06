<h1 align="center">
    ๐จ Useful Things to SCSS
</h1>

<p align="center">
Useful things that I use in SCSS and that make the work easier.
</p>

<p align="center">
<img alt="GitHub language count" src="https://img.shields.io/github/languages/count/AleNoia/useful-things-SCSS?color=%2304D361"> <img alt="Repository size" src="https://img.shields.io/github/repo-size/AleNoia/useful-things-SCSS"> <img alt="License" src="https://img.shields.io/badge/license-MIT-brightgreen"> <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/AleNoia/useful-things-SCSS">
</p>

***

# ๐ Table of Contents

* ๐ก [Features](#features)
* ๐ฏ [Purpose](#Purpose)
* ๐  [Installation](#Installation)
* ๐ [Utilization](#Utilization)
  * ๐ฝ [Reset](#Reset)
  * ๐จ [Colors](#Colors)
  * โ [Shadow](#Shadow)
  * ๐ข [Transition](#Transition)
  * ๐ฆ [Flexbox](#Flex)
  * ๐ฅ [Grid](#Grid)
  * ๐ [Spacing](#Spacing)
  * ๐งฉ [Components](#Components)
* ๐ค [Contributing](#Contributing)
* โ [Technologies Used](#TechnologiesUsed)
* ๐ [Author](#Author)
* ๐งพ [License](#License)

***

# <a name="features"></a>๐ก Features

* ๐ Organization
* ๐ฝ Reset css
* ๐จ Colors
* โ Shadows styles
* ๐ข Transition
* ๐ฆ Simplified Flexbox
* ๐ฅ Simplified grids into classes
* ๐ Spacing classes 
* ๐งฉ Components basics like
    * Buttons and animation style
    * Card
    * Navbar 
    * Navbar vertical
    * Footer
    * Scroll
***

# <a name="Purpose"></a>๐ฏ Purpose

My purpose with this repository is to share my SCSS codes and also receive contributions to grow knowledge.

***

# <a name="Installation"></a>๐  Installation

First you need to download [git](https://git-scm.com) initially

Run this command to clone the repository:

```git

git clone https://github.com/AleNoia/useful-thingss-SCSS.git

```

Run a compiler SCSS like [Live SASS](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)

***

# <a name="Utilization"></a>๐ Utilization

This repository has the purpose of storing SCSS codes, so there are some folder divisions according to each functionality.

```
/usefulScss
 |
 โโโ /Components
 |   โโโ _buttons.scss
 |   โโโ _card.scss
 |   โโโ _footer.scss
 |   โโโ _navbarVertical.scss
 |   โโโ _scroll.scss
 |
 โโโ /Spacing
 |   โโโ _Margin.scss
 |   โโโ _Padding.scss
 |
 โโโ _colors.scss
 โโโ _isFlex.scss
 โโโ _project.scss
 |   ...
 |
 โโโ mainUseful.scss
```

In the ```project``` folder enter your project's codes.

***

## <a name="Reset"></a>๐ฝ Reset

A reset css by [Meyerweb](https://meyerweb.com/eric/tools/css/reset/)

***

## <a name="Colors"></a>๐จ Colors

In colors there are three divisions:

### Colors project

Here you can enter the colors of your project.
```scss
$color-1: #0096c7;
```

### Gradient project

Here you can enter the gradients of your project.
```scss
$gradient-1: linear-gradient(to left top, #8ff8ff, #97f6ff, #a0f4ff, #a8f1ff, #b0efff);
```

### Colors buttons

Default button colors
```scss
$color-primary: linear-gradient(to right bottom, #0069d9, #1374e1, #2280ea, #2f8bf1, #3b97f9);
$color-secondary: hsla(0, 0%, 100%, 0);
$color-success: linear-gradient(to right bottom, #00b027, #09ba2f, #11c536, #17cf3e, #1cda45);
$color-danger: linear-gradient(to right bottom, #c82333, #d53341, #e1424f, #ed505d, #f95d6c);
```

**OBS: It is advisable to follow the "type-color-number" pattern**

*** 

## <a name="Shadow"></a>โ Shadow

Here you can enter the shadows of your project.
```scss
$shadow-1: hsla(0, 0%, 0%, 0.25) 0px 5px 10px;
```

**OBS: It is advisable to follow the "type-shadow-number" pattern**

***

## <a name="Transition"></a>๐ข Transition 

Here you can enter the transitions of your project.

```scss
$transition-1: ease .15s;
```

**OBS: It is advisable to follow the "transition-number" pattern**

*** 

## <a name="Spacing"></a>๐ Spacing

Folder with mixins to assign spacing.

All mixins can receive two variables:

* ```$NumOfClass```  Number of spacings you want to have. 
* ```$SpacingEm```  Spacing size.

### Margin

In margin you will have:

* `.m-NUMBER`   to margin
* `.mx-NUMBER`  to X-axis margin
* `.my-NUMBER`  to Y-axis margin
* `.mt-NUMBER`  to margin top
* `.mb-NUMBER`  to margin bottom
* `.ml-NUMBER`  to margin left
* `.mr-NUMBER`  to margin right

```scss
$NumOfClass: 7;
$SpacingEm: 0.4;

// ================================ Margin
@for $i from 0 through $NumOfClass{
    .m*#{$i * 1}{
        margin: #{$i * $SpacingEm}em;
    }
}
```

#### โ Example:

You will use `m-2` in a class HTML for example.
```html
<div class="card m-2">
    <h1>Card example</h1>
</div>
```

- - - 

### Padding

In padding you will have:

* `.p-NUMBER` to padding
* `.px-NUMBER` to X-axis padding
* `.py-NUMBER` to Y-axis padding
* `.pt-NUMBER` to padding top
* `.pb-NUMBER` to padding bottom
* `.pl-NUMBER` to padding left
* `.pr-NUMBER` to padding right

```scss
$NumOfClass: 7;
$SpacingEm: 0.4;

// ================================ Padding
@for $i from 0 through $NumOfClass{
    .p*#{$i * 1}{
        padding: #{$i * $SpacingEm}em;
    }
}
```

#### โ Example:

You will use `p-2` in HTML for example.
```html
<div class="card p-2">
    <h1>Card example</h1>
</div>
```

## <a name="Flex"></a>๐ฆ Flexbox

Folder with mixins and classes to assign Flexbox.

All mixins can receive two parameters:

* ```$align```
* ```$justify```

### @mixin is-flex / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/PopZjLr)

```scss
// ========== [IS-FLEX]
@mixin is-flex($align, $justify) {
    display: flex;
    align-items: $align;
    justify-content: $justify;
    flex-wrap: wrap;
}
```

#### โ Example:

```scss
body{
  @include is-flex(center, center)
}
```

***

### @mixin is-flex-column / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/LYWGjWM?editors=1100)

```scss
// ========== [IS-FLEX-COLOUMN]
@mixin is-flex-column($align, $justify) {
    display: flex;
    flex-direction: column;
    align-items: $align;
    justify-content: $justify;
}
```

#### โ Example:

```scss
body{
  @include is-flex-column(center, space-around)
}
```

***

### @mixin is-flex-self / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/NWpxMBp?editors=1100)

```scss
// ========== [IS-FLEX-SELF]
@mixin is-flex-self($align, $justify) {
    align-self: $align;
    justify-self: $justify;
}
```

#### โ Example:

```scss
body{
  display: flex;
}
.card{
  @include is-flex-self(center, center)
}
```

***

### .class is-flex / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/JjWGZEj?editors=1100)

```scss
// ========== [IS-FLEX]
.is-flex{
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
}
```

#### โ Example:

```html
<body class="is-flex">
    <div class="card">
        <h1>Card example #1</h1>
    </div>
    <div class="card">
        <h1>Card example #2</h1>
    </div>
</body>
```

***

### .class is-flex-column / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/bGqaXjP?editors=1100)

```scss
// ========== [IS-FLEX-COLUMN]
.is-flex-column{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
}
```

#### โ Example:

```html
<main class="is-flex-column">
  <div class="card ">
    <h1>Card example #1</h1>
  </div>
  <div class="card">
    <h1>Card example #1</h1>
  </div>
</main>
```

***

## <a name="Grid"></a>๐ฅ Grid / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/ExWWbgL?editors=1100)

Customizable grid system

```scss
// ======================================== [VARIABLES]
$grid-gutter: 1%; 
$grid-columns: 12; 
$grid-max: 980px; 

// ======================================== [GRID]
* {
    box-sizing: border-box;
}
[class*="grid-"] {
  float: left;
  margin-bottom: 20px;
  padding: 0 $grid-gutter;
}

@for $i from 1 through $grid-columns{ 
  .grid-#{$i} {
    width: 100% / $grid-columns * $i;
  }
}
```

#### โ Example:
```html
<div class="grid-2">
  <h1>Grid 2</h1>
</div>
<div class="grid-10">
  <h1>Grid 10</h1>
</div>
```

***

## <a name="Components"></a>๐งฉ Components

Basic components


### ๐ Table of Contents
  *  [Buttons](#Buttons)
  *  [Card](#Card)
  *  [Navbar](#nav)
  *  [Scroll](#Scroll)


##

## ๐ <a name="Buttons"></a> Buttons / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/jOBBqKb?editors=1100)

There is a standard class to be a button: ```btn```

```html
<button class="btn btn-primary">Button</button>
```

There are four types of buttons:

### Primary button

```scss
.btn-primary {
    background-image: $color-primary;
}
```

###  Secondary button

```scss
.btn-secondary {
    background-image: $color-secondary;
    color: #343a40;
}
```

###  Success button

```scss
.btn-success {
    background-image: $color-success;
}
```

###  Danger button

```scss
.btn-danger {
    background-image: $color-danger;
}
```

### To up

```scss
.btn-up {

    &:hover {
        box-shadow: $shadow-1;
        transform: scale(1.1);

        i {
            transform: scale(1.2);
        }
    }

    &:active {
        transform: scale(0.99);
        outline: none;
    }
}
```

##

## ๐ <a name="Card"></a> Card / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/QWpQLNN?editors=1100)

Card style

```scss
.card {
    padding: 1em 1.5em;
    border-radius: 13px;
    margin-bottom: .8em;
    box-shadow: $shadow-1;
    background-color: rgb(255, 255, 255);
}
```
##

## ๐ <a name="nav"></a> Navbar 

### Navbar 
Variables:
```scss
$navbarOn: true; //On to spacing main
$heightNavbar: 70px; // Height navbar
```
#### โ Example:
#### SCSS
```scss
.navbar{
    @include navbar-1();
}
```
#### HTML
```html
<nav class="navbar">
    <div class="navbarContent">
        <div class="navBrand mr-4">
            <h1 class="">Brand</h1>
        </div>
        <div class="navbarContentMain">
            <div class="contentStart">
                <a href="./index.html"><button class="btn btn-primary"><i class="fas fa-ticket-alt mr-2"></i>Button Start</button></a>
            </div>
            <div class="contentEnd">
                <a href="./admin.html"><button class="btn btn-primary"><i class="fas fa-crown mr-2"></i>Button End</button></a>
            </div>
        </div>
    </div>
</nav>
```

##

### Navbar Vertical
#### The body and main have to have these settings
```scss
body {
    @include is-flex(flex-start, flex-start);
}

main {
    @extend .grid-9; // According to your grid
}
```
#### โ Example:
#### SCSS
```scss
.navbarVertical{
    @include navbar-vertical-1();
}
```
#### HTML
```html
<nav class="navbarVertical">
    <div class="navbarContent">
        <div class="navBrand">
            <h1>Brand</h1>
        </div>
        <ul class="namesList">
            <button class="btn navItem">Item</button>
        </ul>
    </div>
</nav>
```
##

## ๐ <a name="Footer"></a> Footer 

Simple Footer Style

#### โ Example:

```html
<footer>
    <h1 class="mb-5">
        <strong>Developed</strong> by <a href="https://github.com/AleNoia" class="a" target="_blank">Igor Noia
            Silva</a>
    </h1>
    <div class="footer-buttons">
        <a href="https://github.com/AleNoia" target="_blank" class="mr-2">
            <button class="btn btn-footer">
                <span>Github</span>
            </button>
        </a>
        <a href="https://www.linkedin.com/in/igor-noia-619a0820b/" target="_blank" class="mr-2">
            <button class="btn btn-footer">
                <span>Linkedin</span>
            </button>
        </a>
        <a href="https://github.com/AleNoia/client-manager" target="_blank">
            <button class="btn btn-footer">
                <span>Documentation</span>
            </button>
        </a>
    </div>
</footer>
```

##

## ๐ <a name="Scroll"></a> Scroll 

Scroll style

### Scroll #1 / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/OJpbNQV)

```scss
// ========== [TYPE 1]
@mixin scroll-1() {
  &::-webkit-scrollbar {
    width: .5em;
    background-color: $colorBackground;
  }

  /* Track */
  &::-webkit-scrollbar-track {
    border-radius: .7em;
  }

  /* Handle */
  &::-webkit-scrollbar-thumb {
    background-image: $gradient1;
    cursor: pointer;
  }
}
```

### Scroll #2 / ๐จโ๐ป [Codepen](https://codepen.io/alenoia/pen/PopEMLg)

```scss
// ========== [TYPE 2]
@mixin scroll-2() {
  &::-webkit-scrollbar {
    width: 17px;
    padding: 20px 0;
  }
  
  &::-webkit-scrollbar-thumb {
    background-color: $color-2;
    cursor: pointer;
    border-radius: .7em;
    border: 5px solid transparent;
    background-clip: padding-box;  
  }
}
```


***

# <a name="TechnologiesUsed"></a> โ Technologies used

Technologies that were used in the construction of the project:

- [SCSS](https://sass-lang.com)

***

# <a name="Contributing"></a>๐ค Contributing

1. Fork the project.
2. Create a new branch with your changes: ```git checkout -b my-feature```
3. Save your changes and create a commit message telling you what you did: ```git commit -m" feature: My new feature "```
4. Submit your changes: ```git push origin my-feature```
5. Now just open your pull request in the repository that you forked describing your changes
6. After the merge of your pull request is done, you can delete yout branch

> If you have any questions check [this guide](https://github.com/unform/unform/blob/main/.github/CONTRIBUTING.md) on how to contribute
 
Feel free to contribute ๐

***
# <a name="Author"></a>๐ Author

### [Igor Noia Silva](https://github.com/AleNoia)

If you want to contact, mail me or send a message on Twitter

[![Gmail Badge](https://img.shields.io/badge/-igornoiasilva@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:igornoiasilva@gmail.com)](mailto:igornoiasilva@gmail.com)  ![badge](https://img.shields.io/twitter/url?label=%40IgorNoiaSilva&style=social&url=https%3A%2F%2Ftwitter.com%2FIgorNoiaSilva)

***

# <a name="License"></a>๐งพ License

Released in 2021. This project is under the [MIT license](https://github.com/AleNoia/todolist/blob/main/LICENSE).

Made by [Igor Noia](https://github.com/AleNoia)  โ
