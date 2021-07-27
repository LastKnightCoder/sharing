<template>
  <div class="cardlist">
    <Card
      v-for="(item, i) in counts"
      :key="i"
      :imagesrc="images[i] ? images[i] : 'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/wafer-wan-XAiev-GvCyg-unsplash.47qsrh27dwm0.jpg'"
      :userimage="images[i] ? images[i] : 'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/wafer-wan-XAiev-GvCyg-unsplash.47qsrh27dwm0.jpg'"
      :description="descriptions[i] || 'Hello World'"
      :username="usernames[i] || 'xxx'"
      :viewcount="Math.random().toFixed(3) * 10000"
    />
  </div>
</template>

<script setup>
import Card from './Card.vue'
import { ref } from 'vue'
const props = defineProps({
  counts: {
    default() {
      return new Array(6)
    }
  }
})
const images = [
  'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/kirk-thornton-YIcZBOWmjbM-unsplash.5fq3lt9m1140.jpg',
  'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/mia-baker-jjhvyxm34nY-unsplash.5z9tlu05kbk0.jpg',
  'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/wafer-wan-XAiev-GvCyg-unsplash.47qsrh27dwm0.jpg',
  'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/karsten-winegeart-jqVvBbspJx8-unsplash.30xfypu6ii00.jpg',
  'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/wugui.14bdikpnakv4.jpeg',
  'https://cdn.jsdelivr.net/gh/LastKnightCoder/ImgHosting3@master/shanya.6ko0a5uorqc0.jpeg'
]
const descriptions = ['大庇天下寒士俱欢颜！', '千金散尽还复来！', '寻寻觅觅，冷冷清清，凄凄惨惨戚戚。', '俺老孙来也', '醉里挑灯看剑，梦回吹角连营。', '进一步有进一步的欢喜']
const usernames = ['杜甫', '李白', '李清照', '孙悟空', '辛弃疾', '鸡汤王']

const counts = ref(props.counts)
</script>

<style scoped>
.cardlist {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 10px;
}
</style>