<template>
  <div class="box" ref="box">
    <div class="slider" ref="slider"></div>
    <slot></slot>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const slider = ref(null)
const box = ref(null)

const mouseMove = (event) => {
  const width = parseInt(window.getComputedStyle(box.value).width)
  box.value.style.width = width + event.movementX + 'px'
}
const mouseUp = () => {
  document.removeEventListener('mousemove', mouseMove)
}
const mouseDown = () => {
  document.addEventListener('mousemove', mouseMove)
  document.addEventListener('mouseup', mouseUp)
}

onMounted(() => {
  slider.value.addEventListener('mousedown', mouseDown)
})


</script>

<style scoped>
.box {
  position: relative;
}
.slider {
  width: 20px;
  height: 100%;
  position: absolute;
  top: 0;
  border-radius: 10px;
  right: -10px;
  z-index: 999;
  cursor: col-resize;
}
.slider::after {
  content: '';
  display: block;
  width: 1px;
  height: 100%;
  position: absolute;
  top: 0;
  right: 0px;
  background: white;
  opacity: .1;
  border-radius: 10px;
}
</style>