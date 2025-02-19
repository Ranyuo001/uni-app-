<template>
  <view class="userinfo">
    <!-- <image :src="avatar" mode="" class="avatar"></image> -->
    <image :src="avatar" mode="" class="avatar"></image>
    <view class="username">{{ username }}</view>
  </view>
</template>

<script lang="ts" setup>
import { computed, ref } from "vue"
const props = defineProps(['username', 'avatar'])
// const myname = computed(() => {
//   return props.username
// })
console.log(props);


</script>

<style lang="scss" scoped>
.userinfo {
  width: 100%;
  height: 200px;
  background: #ccc;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  .avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
  }

  .username {
    padding: 10px 0;
    font-size: 20px;
  }
}
</style>