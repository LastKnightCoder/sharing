# 术语介绍

介绍 Grid 布局需要用到的术语



<v-click>

### 容器和子项

<TwoColumn>

<div>

```html
<div class=".container">
  <div class=".item"></div>
  <div class=".item"></div>
  <div class=".item"></div>
  <div class=".item"></div>
</div>
```
</div>

<GridBox 
  :counts="4"
  :style="style[0]"
  :itemStyle="itemStyle[0]"
  :itemStyles="itemStyles[0]"
/>

</TwoColumn>

</v-click>

<v-click>

### 网格线与网格单元

<TwoColumn>

<GridBox
  :counts="6"
  :style="style[1]"
/>

<p style="fontSize: 14px; lineHeight: 1.5">网格通过网格线来进行划分，四个相邻的网格线包围的区域形成一个网格单元。网格线的编号从 <kbd>1</kbd> 开始，我们也可以使用负数，例如 <kbd>-1</kbd> 表示倒数第一根网格线。</p>

</TwoColumn>

</v-click>

<v-click>

### 网格轨道

相邻网格线形成的行和列，我们称之为轨道。

<GridBox
  :counts="9"
  :style="style[2]"
  :itemStyle="itemStyle[2]"
  :itemStyles="itemStyles[2]"
/>

</v-click>


<script setup>

const style = [{
  width: '150px',
  gridTemplateColumns: '1fr 1fr 1fr',
  gridTemplateRows: '50px 50px'
}, {
  width: '150px',
  gridTemplateColumns: '1fr 1fr 1fr',
  gridTemplateRows: '50px 50px'
}, {
  width: '150px',
  gridTemplateColumns: '1fr 1fr 1fr',
  gridTemplateRows: '50px 50px 50px'
}]

const itemStyle = [{
  color: 'white'
}, {}, {
  backgroundColor: 'transparent'
}]

const itemStyles = [[{
  gridRow: '1 / 2',
  gridColumn: '1 / 3',
  backgroundColor: 'rgba(46, 49, 124, .8)',
}, {
  gridRow: 'span 2',
  gridColumn: '3 / 4',
  backgroundColor: '#126bae',
}, {
  backgroundColor: '#0f95b0'
}], [], [{
  backgroundColor: '#ce5577'
}, {
  backgroundColor: '#ce5577'
}, {
  backgroundColor: '#ce5577'
}, {
  backgroundColor: '#ce5577'
}, {}, {}, {
  backgroundColor: '#ce5577'
}]]
</script>