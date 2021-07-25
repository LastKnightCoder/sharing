---
layout: image-left
image: https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/gap-bg.1k8ms7hbfotc.jpeg
---

# gap

通过 <kbd>column-gap</kbd> <kbd>row-gap</kbd> 规定网格之间的间距

通过 <kbd>column-gap</kbd> 与 <kbd>row-gap</kbd> 来控制网格之间的间距

```css
.container {
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 50px);
  column-gap: 10px;
  row-gap: 5px;
}
```

<GridBox
  :counts="7"
  :style="{
    gridTemplateColumns: 'repeat(4, 1fr)',
    gridTemplateRows: 'repeat(2, 50px)',
    columnGap: '10px',
    rowGap: '5px'
  }"
/>

<kbd>gap</kbd> 是 <kbd>column-gap</kbd> 与 <kbd>row-gap</kbd> 的简写形式，因此上面可以简写为如下

```css
.container {
  gap: 10px 5px;
}
```

当 <kbd>gap</kbd> 只指定了一个值时，表示列间距与行间距取同一个值

```css
gap: 10px;
/* 等价于 */
column-gap: 10px;
row-gap: 10px;
```