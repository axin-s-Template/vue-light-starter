<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import Count from '@/components/Count.vue'
import { useCounterStore } from '@/stores/counter'
const counterStore = useCounterStore()

</script>

<template>
  <header>
    <div class="wrapper">
      <h1>Vue 3 + Vite 轻量启动模版项目</h1>
      <nav>
        <RouterLink to="/">主页</RouterLink>
        <RouterLink to="/about">关于</RouterLink>
      </nav>
    </div>
  </header>
  <div class="wrapper">
    <count />
    <h3> 翻倍是：{{ counterStore.doubleCount }} </h3>
    <button style="width: 30px;margin: 0 12px;" @click="counterStore.increment"> + </button>
    <button style="width: 30px;margin: 0 12px;" @click="counterStore.reduce"> - </button>
  </div>
  <RouterView />
</template>

<style scoped></style>
