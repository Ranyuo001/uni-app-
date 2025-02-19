<template>
  <view>
    子组件
    <button @click="onclick">按钮</button>
    <view>--------</view>
    <input type="text" @input="onInput">
  </view>
</template>

<script setup lang="ts">
const emit = defineEmits(['add', 'change'])
function onclick() {
  emit("add", Math.random())
}
function onInput(e) {
  console.log(e.detail.value);
  emit("change", e.detail.value)
}


</script>

<style scoped>
input {
  border: 1px solid #cfcfcf;
  height: 40px;
}
</style>