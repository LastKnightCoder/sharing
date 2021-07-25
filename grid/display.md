---
layout: image-left
image: https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/yixiantian.6aafoagujc80.jpeg
---

# display

默认行为

当我们设置 <kbd>display: grid</kbd> 或者 <kbd>display: inline-grid</kbd> 时，容器就变为了一个网格盒子。

当没有划分网格时，如果没有设定高度，那么默认与块级盒子的行为一致

```css
.container {
  display: grid;
}
```

<GridBox />

设定高度以后，会均匀平分高度

```css
.container {
  height: 160px;
}
```

<GridBox
  :style="{
    height: '160px'
  }"
/>

