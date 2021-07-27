<template>
  <div class="container">
    <div class="img"><img :src="props.imagesrc" alt=""></div>
    <div class="description">{{props.description}}</div>
    <div class="info">
      <div class="user">
        <div class="userimage" :style="{background: `url(${props.userimage}) no-repeat center`, backgroundSize: 'cover'}"></div>
        <div class="username">{{props.username}}</div>
      </div>
      <div class="viewcount">{{props.viewcount}}浏览</div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
img {
  border-radius: 10px;
}
.description {
  height: 4em;
  padding: 1em;
}
.info {
  display: flex;
  justify-content: space-between;
}
.user {
  display: flex;
}
.userimage {
  width: 20px;
  height: 20px;
  border-radius: 50%;
}
.username {
  line-height: 20px;
}
</style>

<script setup>
const props = defineProps({
  imagesrc: {
    default : ''
  },
  description: {
    default: ''
  },
  userimage: {
    default: ''
  },
  username: {
    default: ''
  },
  viewcount: {
    default: 0
  }
})
</script>