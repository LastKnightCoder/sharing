<template>
  <div class="container" :class="[direction, wrap, justify, alignItems, alignContent]" :style="style">
    <div v-for="(item, index) in items" class="item" :key="index" :style="itemStyle">{{index + 1}}</div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const props = defineProps({
  direction: {
    default: 'row'
  },
  wrap: {
    default: 'no-wrap'
  },
  justify: {
    default: 'justify-flex-start'
  },
  alignItems: {
    default: 'align-items-stretch'
  },
  alignContent: {
    default: 'align-content-stretch'
  },
  counts: {
    default: 4
  },
  style: {
    default: function () {
      return {}
    }
  },
  itemStyle: {
    default: function () {
      return {}
    }
  }
})

const direction = ref(props.direction)
const items = ref(new Array(+props.counts))
const wrap = ref(props.wrap)
const justify = ref(props.justify)
const alignItems = ref(props.alignItems)
const alignContent = ref(props.alignContent)
const itemStyle = ref(props.itemStyle)
</script>

<style scoped>

.container {
  display: flex;
}
.item {
  width: 100px;
  height: 100px;
  background-color: #ce5577;
  outline: 1px solid white;
}

/* direction */
.row {
  flex-direction: row;
}
.row-reverse {
  flex-direction: row-reverse;
}
.column {
  flex-direction: column;
}
.column-reverse {
  flex-direction: column-reverse;
}

/* flex-wrap */
.no-wrap {
  flex-wrap: nowrap;
}

.wrap {
  flex-wrap: wrap;
}

.wrap-reverse {
  flex-wrap: wrap-reverse;
}

/* justify-content */
.justify-flex-start {
  justify-content: flex-start;
}

.justify-flex-end {
  justify-content: flex-end;
}

.justify-center {
  justify-content: center;
}

.justify-space-between {
  justify-content: space-between;
}

.justify-space-around {
  justify-content: space-around;
}

.justify-space-evenly {
  justify-content: space-evenly;
}

/* align-items */
.align-items-stretch {
  align-items: stretch;
}
.align-items-flex-start {
  align-items: flex-start;
}
.align-items-flex-end {
  align-items: flex-end;
}
.align-items-center {
  align-items: center;
}

/* align-content */
.align-content-stretch {
  align-content: stretch;
}
.align-content-flex-start {
  align-content: flex-start;
}
.align-content-flex-end {
  align-content: flex-end;
}
.align-content-center {
  align-content: center;
}
.align-content-space-between {
  align-content: space-between;
}
.align-content-space-around {
  align-content: space-around;
}
.align-content-space-evenly {
  align-content: space-evenly;
}
.align-content-baseline {
  align-content: baseline;
}


</style>