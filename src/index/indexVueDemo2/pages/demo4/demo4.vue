<template>
  <view class="">
    <ran_child @add="onAdd" @change="onChange"></ran_child>
    <view class="box" :style="{ background: color, fontSize: size + 'px' }">num:{{ num }}</view>
  </view>
</template>

<script setup lang="ts">
import ran_child from '../../compoents/ran_child/ran_child.vue'
import { ref } from 'vue'
const num = ref(0)
const color = ref('#ccc')
const size = ref(0)
const onAdd = function (e) {
  console.log(e);
  num.value = e
  color.value = "#" + String(e).substring(3, 6)
}
const onChange = function (e) {
  size.value = e
  console.log(e);

}
</script>

<style lang="scss" scoped>
.box {
  width: 200px;
  height: 200px;
}
</style>