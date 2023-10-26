<template>
  <view class="content">
    <button
      type="primary"
      size="mini"
      hover-class="button-hover"
      @click="start"
    >
      开始
    </button>
  </view>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const title = ref('Hello Jiantao')

function start() {
  uni.scanCode({
    success (res) {
      console.log(res)
    },
    fail(data) {
      console.log(data)
    }
  })

}
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
