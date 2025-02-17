<template>
  <view>
    姓名：张三
  </view>
  <view>
    {{ 2 + 3 }}
    {{ num }}
    <button @click="add">num+1</button>
  </view>


  <view>{{ Date.now() }}</view>
  <view>{{ Math.random() }}</view>
  <view>{{ 1 > 2 ? '张三' : num }}</view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
let num = ref(123)

function add() {
  num.value++
}
</script>

<style scoped></style>