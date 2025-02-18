<template>
  <view class="out">
    <!-- 使用 v-bind:class 指令根据 isFocused 的值来动态添加或移除 .active 类 -->
    <input type="text" :value="iptValue" @focus="onfocus" @blur="onBlur">
    <image src="../../../static/chicken.gif" mode="" :class="{ 'pic': true, 'active': isFocused }" @focus="onfocus" />
  </view>
</template>

<script setup lang="ts">
import { ref } from "vue";
const iptValue = ref("123");
// 创建一个响应式变量来跟踪输入框的焦点状态
const isFocused = ref(false);

function onfocus(e) {
  console.log("============", e);
  // 当输入框获得焦点时，将 isFocused 设置为 true
  isFocused.value = true;
}

function onBlur(e) {
  console.log("============", e);
  // 当输入框失去焦点时，将 isFocused 设置为 false
  isFocused.value = false;
}
</script>

<style lang="scss" scoped>
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

.pic {
  width: 24px;
  height: 24px;
  z-index: 1;
  position: absolute;
  top: 0px;
  left: calc(50% - 12px);
  transition: all 0.3s;
}

.pic.active {
  top: -24px;
}
</style>