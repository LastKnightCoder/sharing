<template>
  <div class="container" :style="containerStyle">
    <div v-for="(item, index) in items" class="item" :style="[itemStyle, itemStyles[index]]" :key="index">
      {{itemContents[index] ?? (index + 1)}}
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const props = defineProps({
  containerStyle: {
    default: function() {
      return {}
    }
  },
  itemStyle: {
    default: function() {
      return {}
    }
  },
  itemStyles: {
    default: function() {
      return []
    }
  },
  itemContents: {
    default: function() {
      return []
    }
  },
  counts: {
    default: 4
  }
})
const containerStyle = ref(props.containerStyle)
const itemStyle = ref(props.itemStyle)
const itemStyles = ref(props.itemStyles)
const itemContents = ref(props.itemContents)
const items = ref(new Array(props.counts))
</script>

<style scoped>
.container {
  display: grid;
  outline: 1px solid #7a7374;
}
.item {
  box-sizing: border-box;
  border: 1px solid white;
  background-color: #ce5577;
  border-radius: 5px;
  /* outline: 1px solid white; */
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>