<template>
  <view class="">
    <ran_layout>
      <template #header>
        首页头部
      </template>
      <template #main>
        <view class="box1"></view>
      </template>
    </ran_layout>
  </view>
</template>

<script setup lang="ts">
import ran_layout from '../../compoents/ran_layout/ran_layout.vue'

</script>

<style lang="scss" scoped>
.box1 {
  width: 100px;
  height: 100px;
  background: pink;
}

.box2 {
  width: 120px;
  height: 120px;
  background: skyblue;
}
</style>