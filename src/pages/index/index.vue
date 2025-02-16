<template>
  <view class="layout">
    <view class="box1">{{ title1 }}</view>
    <view class="box2">{{ title2 }}</view>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const title1 = ref('Hello')
const title2 = ref('World')
</script>

<style lang="scss">
.layout {
  border: 1px solid red;

  .box1 {
    border: 1px solid blue;
  }

  .box2 {
    border: 1px solid green;
  }
}
</style>
