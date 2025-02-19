<template>
  <view class="userinfo">
    <!-- <image :src="avatar" mode="" class="avatar"></image> -->
    <!-- <image :src="avatar" mode="" class="avatar"></image>
    <view class="username">{{ username }}</view> -->
    <image :src="obj.avatar" mode="scaleToFill" class="avatar" />
    <view>{{ obj.username }}</view>
  </view>
</template>

<script lang="ts" setup>
import { computed, ref } from "vue"
// const props = defineProps(['username', 'avatar'])
// const myname = computed(() => {
//   return props.username
// })

// const props = defineProps({
//   username: {
//     type: String,
//     default: '匿名'
//   },
//   avatar: {
//     type: String,
//     default: '../../../../static/logo.png'
//   }
// })
defineProps({
  obj: {
    type: Object,
    default: () => {
      return {
        username: '匿名',
        avatar: '../../../../static/logo.png'
      }
    }
  }
})


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