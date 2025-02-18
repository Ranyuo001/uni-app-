<template>
  <view class="out">
    <input type="text" v-model="firsName" placeholder="请输入名">
    <input type="text" v-model="lastName" placeholder="请输入姓">
    <view>全称：{{ firsName }}--{{ lastName }}</view>
    <view>全称：{{ fullName }}</view>
  </view>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue'
const firsName = ref('')
const lastName = ref('')

const fullName = computed(() => {
  return firsName.value + '--' + lastName.value
})
</script>

<style scoped lang="scss">
.out {
  padding: 20px;

  input {
    border: 1px solid #ccc;
    height: 40px;
    margin: 10px 0;
    padding: 0 10px;
  }
}
</style>