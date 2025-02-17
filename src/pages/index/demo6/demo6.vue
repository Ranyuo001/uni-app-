<template>
  <view v-if="true">
    京东
  </view>
  <view v-else>
    淘宝
  </view>
  <view @click="shop = !shop">
    {{ shop ? '京东' : '淘宝' }}
  </view>
  <!-- 使用 v-model 绑定输入框的值 -->
  <input type="text" v-model.number="day">
  <view v-if="day === 1">星期一</view>
  <view v-else-if="day === 2">星期二</view>
  <view v-else-if="day === 3">星期三</view>
  <view v-else-if="day === 4">星期四</view>
  <view v-else-if="day === 5">星期五</view>
  <view v-else-if="day === 6">星期六</view>
  <view v-else-if="day === 7">星期日</view>
  <view v-else>格式错误</view>

  <view class="box1" v-if="true">box1</view>
  <view class="box2" v-show="true">box2</view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
let shop = ref(true);
let day = ref(2);
</script>

<style scoped lang="scss"></style>