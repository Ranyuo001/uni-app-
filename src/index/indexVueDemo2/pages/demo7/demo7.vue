<template>
  <view>姓名：{{ name }}--{{ age }}</view>
  <scroll-view scroll-y ref="scroll">
    <navigator open-type="reLaunch" url="../demo6/demo6">
      跳转到demo6
    </navigator>
    <view v-if="flag" class="out">↑</view>
    <view v-for="item in 50">{{ item }}</view>

  </scroll-view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { onReady, onLoad, onShow, onHide, onUnload, onPageScroll } from '@dcloudio/uni-app';
const name = ref('张三')
const age = ref('18');
const scroll = ref(null);
const flag = ref(false);
onLoad((e) => {
  console.log('onLoad');
  console.log(e);
  name.value = e!.name
  age.value = e!.age
});

onReady(() => {
  console.log('onReady');
  console.log(scroll.value);
})

onShow(() => {
  console.log('onShow');
})

onHide(() => {
  console.log('onHide');
})

onUnload(() => {
  console.log('卸载页面');
})

onPageScroll((e) => {
  console.log('滚动事件');
  console.log(e);
  flag.value = e.scrollTop > 200
})

</script>

<style scoped>
.out {
  height: 100px;
  width: 100px;
  border-radius: 100%;
  background: skyblue;
  position: fixed;
  right: 30px;
  bottom: 30px;
  text-align: center;
  line-height: 100px;
  font-size: 30px;
}
</style>