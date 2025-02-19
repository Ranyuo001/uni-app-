<template>
  <view class="content">
    <!-- <UserInfo :username="xxm" avatar="../../../../static/pic1.jpg"></UserInfo>
    <UserInfo avatar="../../../../static/pic2.jpg"></UserInfo>
    <UserInfo :username="Zhangsan"></UserInfo> -->
    <UserInfo v-for="(item, index) in userinfo" :obj="item" :key="index"></UserInfo>
  </view>
</template>

<script setup lang="ts">
import UserInfo from '../../compoents/UserInfo/UserInfo.vue'
// import xxm_header from '../../compoents/xxm_header/xxm_header.vue'
import { ref } from 'vue'
const xxm = ref('xxm')
const Lisi = ref('李四')
const Zhangsan = ref('张三')
const userinfo = ref([{
  username: '张三',
  avatar: '../../../../static/pic1.jpg'
},
{
  username: '李四',
  avatar: '../../../../static/pic2.jpg'
},
{
  username: '王五',
  avatar: '../../../../static/pic3.jpg'
},
])
</script>
<style lang="scss" scoped></style>