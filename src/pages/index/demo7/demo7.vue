<template>
  <view class="out">
    <checkbox-group @change="itemChange">
      <view class="item" v-for="(item, index) in goods" :key="item.id">
        <checkbox :value="item.id" :checked="item.checked" />
        <text class="title">{{ item.title }}</text>
        <text class="pirce">{{ item.price }}元</text>
        <text class="del" @click="remove(index)">删除</text>
      </view>
    </checkbox-group>


    <view class="card">
      <view class="text">选择中{{ selectGroup.length }}个产品，总价：{{ computedPrice }}元</view>
    </view>
  </view>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue'
const goods = ref([
  { id: 'qwqwq01', title: '小米', checked: true, price: 1999 },
  { id: 'qwqwq02', title: '华为', checked: false, price: 5999 },
  { id: 'qwqwq03', title: '苹果', checked: false, price: 8999 }
])
const selectGroup = ref([])
const computedPrice = computed(() => {
  return goods.value.filter(item => item.checked).reduce((prev, curr) => prev + curr.price, 0)
})
function remove(index: number) {
  goods.value.splice(index, 1)
}

function itemChange(e: any) {
  selectGroup.value = e.detail.value
  goods.value.forEach(item => {
    item.checked = selectGroup.value.includes(item.id)
  })
}
</script>

<style lang="scss" scoped>
.out {
  padding: 10px;

  .item {
    padding: 10px 0;

    .pirce {
      margin-left: 10px;
    }

    .del {
      color: #c00;
      margin-left: 30px;
    }
  }

  .card {
    padding: 10px;
    background-color: #eee;
    margin-top: 10px;

    .text {
      color: #c00;
    }
  }
}
</style>