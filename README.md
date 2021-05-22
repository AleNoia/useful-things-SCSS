# 🎨 Useful Things to SCSS

Useful things that I use in SCSS and that make the job easier.

If you have any question, suggestion or want to contact, mail me:

📧 igornoiasilva@gmail.com.

***

# 📌 Table of Contents

* 💡 [Features](#features)
* 🎯 [Purpose](#Purpose)
* 🛠 [Installation](#Installation)
* 📝 [Utilization](#Utilization)
  * 💽 [Reset](#Reset)
  * 🎨 [Colors](#Colors)
  * ☂ [Shadow](#Shadow)
  * ✅ [Buttons](#Buttons)
  * 🎢 [Transition](#Transition)
  * 📦 [Flexbox](#Flex)
  * 🖥 [Grid](#Grid)
  * 📏 [Spacing](#Spacing)
  * 🧩 [Components](#Components)
* 🤝 [Contributing](#Contributing)
* 🧾 [License](#License)

***

# <a name="features"></a>💡 Features

* 📦 Simplified Flexbox
* 📏 Spacing classes 
***

# <a name="Purpose"></a>🎯 Purpose

My purpose with this repository is to share my SCSS codes and also receive contributions to grow knowledge.

***

# <a name="Installation"></a>🛠 Installation

Run this command to clone the repository:

```git

git clone https://github.com/AleNoia/useful-thingss-SCSS.git

```

***

# <a name="Utilization"></a>📝 Utilization

This repository has the purpose of storing SCSS codes, so there are some folder divisions according to each functionality.

```
/usefulScss
 |
 ├── /Components
 |   ├── _Scroll.scss
 |
 ├── /Spacing
 |   ├── _Margin.scss
 |   ├── _Padding.scss
 |
 ├── _buttons.scss
 ├── _colors.scss
 ├── _isFlex.scss
 |   ...
 |
 └── mainUseful.scss
```
***

## <a name="Reset"></a>💽 Reset

A reset css by [Meyerweb](https://meyerweb.com/eric/tools/css/reset/)

***

## <a name="Colors"></a>🎨 Colors

In colors there are three divisions:

### Colors project

Here you can enter the colors of your project.
```scss
$color-1: #0096c7;
```

### Gradient project

Here you can enter the gradients of your project.
```scss
$color-1: #0096c7;
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

## <a name="Shadow"></a>☂ Shadow

Here you can enter the shadows of your project.
```scss
$shadow-1: hsla(0, 0%, 0%, 0.25) 0px 5px 10px;
```

**OBS: It is advisable to follow the "type-shadow-number" pattern**

***

## <a name="Buttons"></a>✅ Buttons / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/jOBBqKb?editors=1100)

There is a standard class to be a button: ```btn```

```html
<button class="btn">Button</button>
```

There are four types of buttons:

### Primary button

```scss
// ========== [PRIMARY]
.btn-primary {
    background-image: $color-primary;
}
```

### Secondary button

```scss
// ========== [SECONDARY]
.btn-secondary {
    background-image: $color-secondary;
    color: #343a40;
}
```

### Success button

```scss
// ========== [SUCCESS]
.btn-success {
    background-image: $color-success;
}
```

### Danger button

```scss
// ========== [DANGER]
.btn-danger {
    background-image: $color-danger;
}
```

### To up

```scss
// ========== [TO UP]
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

*** 

## <a name="Spacing"></a>📏 Spacing

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

#### ✏ Example:

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

#### ✏ Example:

You will use `p-2` in HTML for example.
```html
<div class="card p-2">
    <h1>Card example</h1>
</div>
```

## <a name="Flex"></a>📦 Flexbox

Folder with mixins and classes to assign Flexbox.

All mixins can receive two parameters:

* ```$align```
* ```$justify```

### @mixin is-flex / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/PopZjLr)

```scss
@mixin is-flex($align, $justify) {
    display: flex;
    align-items: $align;
    justify-content: $justify;
    flex-wrap: wrap;
}
```

#### ✏ Example:

```scss
body{
  @include is-flex(center, center)
}
```

***

### @mixin is-flex-column / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/LYWGjWM?editors=1100)

```scss
@mixin is-flex-column($align, $justify) {
    display: flex;
    flex-direction: column;
    align-items: $align;
    justify-content: $justify;
}
```

#### ✏ Example:

```scss
body{
  @include is-flex-column(center, space-around)
}
```

***

### @mixin is-flex-self / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/NWpxMBp?editors=1100)

```scss
@mixin is-flex-self($align, $justify) {
    align-self: $align;
    justify-self: $justify;
}
```

#### ✏ Example:

```scss
body{
  display: flex;
}
.card{
  @include is-flex-self(center, center)
}
```

***

### .class is-flex / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/JjWGZEj?editors=1100)

```scss
.is-flex{
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
}
```

#### ✏ Example:

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

## <a name="Components"></a>🧩 Components

Basic components


### 📌 Table of Contents
  * 🖱 [Scroll](#Scroll)

## <a name="Scroll"></a>🖱 Scroll 

Scroll style

### 📍 Scroll #1 / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/OJpbNQV)

```scss
//================================================================ [VARIABLES]
$colorBackground: #fff9dc;
$gradient1: linear-gradient(to right top, #ff930a, #fd7328, #f5543c, #e6344c, #d1105a);

//================================================================ [SCROLL]
@mixin scroll1() {
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



***

# <a name="Contributing"></a>🤝 Contributing

Feel free to contribute 🙂

***

# <a name="License"></a>🧾 License

Released in 2021. This project is under the [MIT license](https://github.com/AleNoia/todolist/blob/main/LICENSE).

Made by [Igor Noia](https://github.com/AleNoia)  ✌
