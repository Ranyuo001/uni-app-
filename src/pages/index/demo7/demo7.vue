<template>
  <view class="out">
    <view class="item" v-for="(item, index) in goods" :key="item.id">
      <checkbox :checked="item.checked" />
      <text class="title">{{ item.title }}</text>
      <text class="del" @click="remove(index)">删除</text>
    </view>
  </view>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
const goods = ref([
  { id: 'qwqwq01', title: '小米', checked: true },
  { id: 'qwqwq02', title: '华为', checked: false },
  { id: 'qwqwq03', title: '苹果', checked: false }
])

function remove(index: number) {
  goods.value.splice(index, 1)
}
</script>

<style lang="scss" scoped>
.out {
  padding: 10px;

  .item {
    padding: 10px 0;

    .del {
      color: #c00;
      margin-left: 30px;
    }
  }
}
</style>