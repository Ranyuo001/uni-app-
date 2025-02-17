<template>
  <view class="box" @click="onclick" :style="{ background: color }">
    {{ num }}
  </view>
  <switch :checked="false" @change="onChange" />
  <button type="primary" :loading="isLoading"> 11</button>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const color = ref('#fc359a')
const num = ref(1)

const isLoading = ref(false)
function onclick() {
  num.value += 1
  color.value = '#' + String(Math.random()).substring(3, 9);
}

function onChange(e: any) {
  isLoading.value = e.detail.value
  console.log(e.target.value)
}
</script>

<style scoped>
.box {
  width: 200px;
  height: 200px;
  background-color: skyblue;
}
</style>