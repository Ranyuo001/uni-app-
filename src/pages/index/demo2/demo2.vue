<template>
  <view>
    <button size="mini" plain="false" loading="false">
      按钮
    </button>
    <input maxlength="14" type="tel" placeholder="搜索内容" placeholder-class="iptClass">
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'

</script>

<style scoped>
.iptClass {
  color: red;
}
</style>