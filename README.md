# 🎨 Useful Things to SCSS

Useful things that I use in SCSS and that make the job easier.

If you have any question, suggestion or want to contact, mail me:

📧 igornoiasilva@gmail.com.

---

# 📌 Table of Contents

- 💡 [Features](#features)
- 🎯 [Purpose](#Purpose)
- 🛠 [Installation](#Installation)
- 📝 [Utilization](#Utilization)
  - 📏 [Spacing](#Spacing)
  - 📦 [Flexbox](#Flex)
  - 🧩 [Components](#Components)
- 🤝 [Contributing](#Contributing)
- 🧾 [License](#License)

---

# <a name="features"></a>💡 Features

- 📦 Simplified Flexbox
- 📏 Spacing classes

---

# <a name="Purpose"></a>🎯 Purpose

My purpose with this repository is to share my SCSS codes and also receive contributions to grow knowledge.

---

# <a name="Installation"></a>🛠 Installation

Run this command to clone the repository:

```git

git clone https://github.com/AleNoia/useful-thingss-SCSS.git

```

---

# <a name="Utilization"></a>📝 Utilization

This repository has the purpose of storing SCSS codes, so there are some folder divisions according to each functionality.

```
/usefulScss
 |
 ├── /Components
 |   ├── /Scroll.scss
 |       ├── Scroll.scss
 |
 ├── /Flex
 |   ├── _isFLex.scss
 |
 ├── /Spacing
 |   ├── _Margin.scss
 |   ├── _Padding.scss
 |
 └── Main.scss
```

## <a name="Spacing"></a>📏 Spacing

Folder with mixins to assign spacing.

All mixins can receive two variables:

- `$NumOfClass` Number of spacings you want to have.
- `$SpacingEm` Spacing size.

### Margin

In margin you will have:

- `.m-NUMBER` to margin
- `.mx-NUMBER` to X-axis margin
- `.my-NUMBER` to Y-axis margin
- `.mt-NUMBER` to margin top
- `.mb-NUMBER` to margin bottom
- `.ml-NUMBER` to margin left
- `.mr-NUMBER` to margin right

```scss
$NumOfClass: 7;
$SpacingEm: 0.4;

// ================================ Margin
@for $i from 0 through $NumOfClass {
  .m*#{$i * 1} {
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

---

### Padding

In padding you will have:

- `.p-NUMBER` to padding
- `.px-NUMBER` to X-axis padding
- `.py-NUMBER` to Y-axis padding
- `.pt-NUMBER` to padding top
- `.pb-NUMBER` to padding bottom
- `.pl-NUMBER` to padding left
- `.pr-NUMBER` to padding right

```scss
$NumOfClass: 7;
$SpacingEm: 0.4;

// ================================ Padding
@for $i from 0 through $NumOfClass {
  .p*#{$i * 1} {
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

- `$align`
- `$justify`

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
body {
  @include is-flex(center, center);
}
```

---

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
body {
  @include is-flex-column(center, space-around);
}
```

---

### @mixin is-flex-self / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/NWpxMBp?editors=1100)

```scss
@mixin is-flex-self($align, $justify) {
  align-self: $align;
  justify-self: $justify;
}
```

#### ✏ Example:

```scss
body {
  display: flex;
}
.card {
  @include is-flex-self(center, center);
}
```

---

### .class is-flex / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/JjWGZEj?editors=1100)

```scss
.is-flex {
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

---

## <a name="Components"></a>🧩 Components

Basic components

- 🖱 [Scroll](#Scroll)

## <a name="Scroll"></a>🖱 Scroll

Scroll style

### 📍 Scroll #1 / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/OJpbNQV)

```scss
//================================================================ [VARIABLES]
$colorBackground: #fff9dc;
$gradient1: linear-gradient(
  to right top,
  #ff930a,
  #fd7328,
  #f5543c,
  #e6344c,
  #d1105a
);

//================================================================ [SCROLL]
@mixin scroll() {
  &::-webkit-scrollbar {
    width: 0.5em;
    background-color: $colorBackground;
  }

  /* Track */
  &::-webkit-scrollbar-track {
    border-radius: 0.7em;
  }

  /* Handle */
  &::-webkit-scrollbar-thumb {
    background-image: $gradient1;
    cursor: pointer;
  }
}
```

---

## <a name="Components"></a>🧩 Components

Basic components

- 🖱 [Scroll](#Scroll)

## <a name="Scroll"></a>🖱 Scroll

Scroll style

### 📍 Scroll #1 / 👨‍💻 [Codepen](https://codepen.io/alenoia/pen/OJpbNQV)

```scss
//================================================================ [VARIABLES]
$colorBackground: #fff9dc;
$gradient1: linear-gradient(
  to right top,
  #ff930a,
  #fd7328,
  #f5543c,
  #e6344c,
  #d1105a
);

//================================================================ [SCROLL]
@mixin scroll() {
  &::-webkit-scrollbar {
    width: 0.5em;
    background-color: $colorBackground;
  }

  /* Track */
  &::-webkit-scrollbar-track {
    border-radius: 0.7em;
  }

  /* Handle */
  &::-webkit-scrollbar-thumb {
    background-image: $gradient1;
    cursor: pointer;
  }
}
```

---

# <a name="Contributing"></a>🤝 Contributing

Feel free to contribute 🙂

---

# <a name="License"></a>🧾 License

Released in 2021. This project is under the [MIT license](https://github.com/AleNoia/todolist/blob/main/LICENSE).

Made by [Igor Noia](https://github.com/AleNoia) ✌
