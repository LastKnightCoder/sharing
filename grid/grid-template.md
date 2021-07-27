<div style="display: grid; grid-template-columns: 2fr 1fr; height: 100%; gap: 20px;">

<div>

# grid-template、grid

属性简写

<kbd>grid-template</kbd> 是 <kbd>grid-template-columns</kbd> <kbd>grid-template-rows</kbd> <kbd>grid-template-areas</kbd> 这三个属性的简写形式。

```css
grid-template: [header-start] 'side header' 75px
                              'side main' auto
                              'side footer' 50px / 100px 1fr
```

<GridBox
  :style="style"
  :itemStyles="itemStyles"
  :itemContents="['header', 'main', 'side', 'footer']"
/>

<kbd>grid</kbd> 属性是 <kbd>grid-template-rows</kbd>、<kbd>grid-template-columns</kbd>、<kbd>grid-template-areas</kbd>、 <kbd>grid-auto-rows</kbd>、<kbd>grid-auto-columns</kbd>、<kbd>grid-auto-flow</kbd> 这六个属性的合并简写形式。

写法太复杂了，没学会...

</div>

<!-- <div style="background: url('https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/gridhsorthand.78pb54imepc0.jpeg') no-repeat center; backgroundSize: cover;"> -->

<!-- </div> -->

</div>

<script setup>
const style = {
  width: '80%',
  gridTemplate: "'side header' 75px 'side main' auto 'side footer' 50px \/ 100px 1fr",
  gap: '5px'
}
const itemStyles = [{
  gridArea: 'header',
  backgroundColor: '#55bb8a'
}, {
  gridArea: 'main',
  height: '200px',
  backgroundColor: '#475164'
}, {
  gridArea: 'side',
  backgroundColor: '#5698c3'
}, {
  gridArea: 'footer',
  backgroundColor: '#8076a3'
}]
</script>