<template>
  <view class="layout">
    <scroll-view scroll-y="true" ref="scroll">
      <view>11</view>
    </scroll-view>
    <life_demo v-if="show"></life_demo>
  </view>
</template>

<script setup lang="ts">
import life_demo from '../../compoents/life_demo/life_demo.vue'
import { ref, onUnmounted, onMounted } from 'vue'
const show = ref(true);
const scroll = ref(null);

setTimeout(() => {
  show.value = false
}, 2000)

</script>

<style scoped></style>