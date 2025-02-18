<template >
  <view class="out">
    <input type="text" :value="iptValue" @input="e => iptValue = (e.target as HTMLInputElement).value"
      @confirm="onConfirm">

    <view>预览:{{ iptValue }}</view>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const iptValue = ref('')
function onConfirm(e) {
  console.log(e);
}
</script>

<style scoped lang="scss">
.out {
  padding: 0 20px;
  margin-top: 40px;
  position: relative;
}

input {

  height: 40px;
  border: 1px solid #ccc;
  position: relative;
  z-index: 2;
  background: #fff;
  padding: 0 10px;
}
</style>