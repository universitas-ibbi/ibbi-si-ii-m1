---
title: Responsive Web with Bootstrap
version: 1.0.0
theme: default
header: Responsive Web with Bootstrap
footer: https://github.com/universitas-ibbi/ibbi-si-ii-m1
paginate: true
marp: true
---

<!--
_class: lead
_paginate: skip
-->

# Responsive Web with Bootstrap

![bg right](./images/pertemuan-8-rwd.gif)

---

Bootstrap 5 provides a wide range of **responsive utility classes** that help you control layout and styling across different screen sizes. These classes typically follow the format:

```
{property}-{breakpoint}-{value}
```

---

### ✅ **Available Breakpoints in Bootstrap 5**

| Breakpoint  | Prefix      | Min Width |
| ----------- | ----------- | --------- |
| Extra small | `""` (none) | `<576px`  |
| Small       | `sm`        | `≥576px`  |
| Medium      | `md`        | `≥768px`  |
| Large       | `lg`        | `≥992px`  |
| Extra large | `xl`        | `≥1200px` |
| XXL         | `xxl`       | `≥1400px` |

---

## 🔧 **List of Responsive Utility Classes**

Below are grouped responsive class categories with examples:

---

## float

Toggle floats on any element, across any breakpoint, using our responsive float utilities.

```html
<div class="float-start">Float start on all viewport sizes</div>
<br />
<div class="float-end">Float end on all viewport sizes</div>
<br />
<div class="float-none">Don’t float on all viewport sizes</div>
```

```HTML
<div class="float-sm-end">Float end on viewports sized SM (small) or wider</div><br>
<div class="float-md-end">Float end on viewports sized MD (medium) or wider</div><br>
<div class="float-lg-end">Float end on viewports sized LG (large) or wider</div><br>
<div class="float-xl-end">Float end on viewports sized XL (extra large) or wider</div><br>
<div class="float-xxl-end">Float end on viewports sized XXL (extra extra large) or wider</div><br>
```

---

## images

Images in Bootstrap are made responsive with .img-fluid. This applies max-width: 100%; and height: auto; to the image so that it scales with the parent width.

```html
<img src="..." class="img-fluid" alt="..." />
```

---

## sticky top

Position an element at the top of the viewport, from edge to edge, but only after you scroll past it.

```html
<div class="sticky-sm-top">
  Stick to the top on viewports sized SM (small) or wider
</div>
<div class="sticky-md-top">
  Stick to the top on viewports sized MD (medium) or wider
</div>
<div class="sticky-lg-top">
  Stick to the top on viewports sized LG (large) or wider
</div>
<div class="sticky-xl-top">
  Stick to the top on viewports sized XL (extra-large) or wider
</div>
<div class="sticky-xxl-top">
  Stick to the top on viewports sized XXL (extra-extra-large) or wider
</div>
```

## sticky bottom

Position an element at the bottom of the viewport, from edge to edge, but only after you scroll past it.

```html
<div class="sticky-sm-bottom">
  Stick to the bottom on viewports sized SM (small) or wider
</div>
<div class="sticky-md-bottom">
  Stick to the bottom on viewports sized MD (medium) or wider
</div>
<div class="sticky-lg-bottom">
  Stick to the bottom on viewports sized LG (large) or wider
</div>
<div class="sticky-xl-bottom">
  Stick to the bottom on viewports sized XL (extra-large) or wider
</div>
<div class="sticky-xxl-bottom">
  Stick to the bottom on viewports sized XXL (extra-extra-large) or wider
</div>
```

---

## container

Containers are a fundamental building block of Bootstrap that contain, pad, and align your content within a given device or viewport.

```html
<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>
```

---

## table

Responsive tables allow tables to be scrolled horizontally with ease.

```html
<div class="table-responsive">
  <table class="table">
    ...
  </table>
</div>
```

Use `.table-responsive{-sm|-md|-lg|-xl|-xxl}` as needed to create responsive tables up to a particular breakpoint. From that breakpoint and up, the table will behave normally and not scroll horizontally.

---

## grid

```html
.col-sm-* .col-md-* .col-lg-* .col-xl-* .col-xxl-*
```
