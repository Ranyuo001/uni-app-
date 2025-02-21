<template>
  <view class="out">
    子组件count值:{{ count }}
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const count = ref(100)
const updateCount = function () {
  count.value++
}
defineExpose({
  count,
  str: 'ranyuo',
  updateCount
})
</script>

<style scoped lang="scss">
.out {
  padding: 20px;
  background: #eee;
}
</style>