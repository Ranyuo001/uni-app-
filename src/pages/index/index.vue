<template>
  <view class="box1" hover-class="boxHover">
    <view class="inner" hover-class="innerHover" hover-stop-propagation>内部元素</view>
  </view>

  <view>---------</view>

  <swiper indicator-dots="false" indicator-color="rgba(0, 0, 0, .3)" indicator-active-color="rgba(255,255,255,0.5)"
    circular="false" autoplay interval="2000" vertical="false">
    <swiper-item v-for="(item, index) in 5" :key="index">
      <view class="box">{{ item }}</view>
    </swiper-item>
  </swiper>

  <view>---------</view>

  <scroll-view class="scrollView" scroll-x="true">
    <view class="box">1</view>
    <view class="box">2</view>
    <view class="box">3</view>
    <view class="box">4</view>
    <view class="box">5</view>

  </scroll-view>


  <view>---------</view>

  <view>
    <navigator url="demo1/demo1" open-type="reLaunch" class="demoList">
      跳转到demo1(基础组件)
    </navigator>
    <navigator url="demo2/demo2" open-type="reLaunch" class="demoList">
      跳转到demo2(按钮组件)
    </navigator>
    <navigator url="demo3/demo3" open-type="reLaunch" class="demoList">
      跳转到demo3(vue3语法)
    </navigator>
    <navigator url="demo4/demo4" open-type="reLaunch" class="demoList">
      跳转到demo4(vue3语法)
    </navigator>
    <navigator url="demo5/demo5" open-type="reLaunch" class="demoList">
      跳转到demo5(vue3语法)
    </navigator>
    <navigator url="demo6/demo6" open-type="reLaunch" class="demoList">
      跳转到demo6(vue3语法)
    </navigator>
    <navigator url="demo7/demo7" open-type="reLaunch" class="demoList">
      跳转到demo7(vue3语法)
    </navigator>
    <navigator url="demo8/demo8" open-type="reLaunch" class="demoList">
      跳转到demo8(小鸡案例)
    </navigator>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const title1 = ref('Hello')
const title2 = ref('World')
</script>

<style lang="scss">
.pic1 {
  width: 100px;
  height: 100px;
}

.pic2 {
  width: 100px;
  height: 100px;
}

.pic3 {
  width: 200px;

}

.pic4 {

  height: 50px;
}

swiper {
  widows: 100vw;
  height: 200px;
  border: 1px solid red;

  swiper-item {
    width: 100%;
    height: 100%;
    background: pink;
  }

  swiper-item:nth-child(2n) {
    background: skyblue;
  }
}

.scrollView {
  width: 80%;
  height: 220px;
  border: 1px solid red;
  white-space: nowrap;
  margin: 10px auto;
}

.box {
  display: inline-block;
  width: 100px;
  height: 100px;
  background: pink;
}

.demoList {
  display: block;
  width: 100%;
  height: 50px;
  border: 1xp solid #ebebeb;
  text-align: center;
  line-height: 50px;
  background-color: rgba(129, 129, 129, 0.05);
}
</style>
