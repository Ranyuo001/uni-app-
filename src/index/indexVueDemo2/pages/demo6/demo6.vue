<template>
  <view class="layout">
    <demo_child ref="child"></demo_child>
    <view>------</view>
    <button @click="() => update">点击修改子值</button>
    <navigator url="../demo7/demo7?name=王五&age=20">
      跳转到demo7
    </navigator>
    <view>-------</view>
    <navigator url="../demo5/demo5">
      跳转到demo5
    </navigator>

  </view>
</template>

<script setup lang="ts">
import demo_child from '../../compoents/demo_child/demo_child.vue'
import { ref, onMounted } from 'vue'
// 假设 demo_child 组件实例类型为 DemoChildInstance
interface DemoChildInstance {
  updateCount: () => void;
}
const child = ref<DemoChildInstance | null>(null)
console.log(child.value);
onMounted(() => {
  console.log(child.value);
})
const update = function () {
  child.value?.updateCount()
}
</script>

<style scoped></style>