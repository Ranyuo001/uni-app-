<template>
  <view>
    <view v-for="(item, index) in arrs" :key="item.id">
      <image :src="item.picurl" />
    </view>
    <button :loading="true">按钮</button>
    <view class="box" :class="{ active: isActive }">
      v-bind指令
    </view>

    <!-- <view class="box" :class="isActive ? 'active' : ' '"></view> -->

    <view :style="{ width: '300px', height: 260 + 'px', fontSize: size + 'px' }" class="box">内联样式</view>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const isActive = ref(false)
let size = ref(30)
const arrs = ref([
  { id: '1', picurl: '../../../static/logo.png' },
  { id: '2', picurl: '../../../static/logo.png' },
])

setInterval(() => {
  isActive.value = !isActive.value
  size.value++
}, 1000)

</script>

<style scoped lang="scss">
.box {
  width: 200px;
  height: 200px;
  background-color: skyblue;
}

.active {
  background-color: red;
  font-size: 50px;
}
</style>