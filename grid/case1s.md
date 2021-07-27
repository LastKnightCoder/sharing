---
layout: image-right
image: https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/kirk-thornton-YIcZBOWmjbM-unsplash.5fq3lt9m1140.jpg
---

<div  class="-mt-6">

```html
<div class="container_wrapper">
  <div class=".container">
    <div class="prose"></div>
    <div class="sidebar">
      <div class="box"></div>
      <div class="box"></div>
    </div>
    <div class="prose"></div>
  </div>
</div>
```

```css
.container_wrapper {
  contain: style layout inline-size;
}
.container {
  display: grid;
  gap: 20px;
}
.sidebar {
  display: inherit;
  gap: inherit;
}

@container (min-width: 600px) and (max-width: 900px) {
  .sidebar {
    grid-template-columns: repear(2, 1fr);
  }
}

@container (min-width: 900px) {
  .container {
    grid-template-columns: 2fr 1fr;
  }
  .sidebar {
    grid-row: span 2;
    grid-auto-rows: min-content;
  }
}
```

</div>