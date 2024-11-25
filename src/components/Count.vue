<template>
  <h2>
    {{ counterStore.count }}
  </h2>
</template>

<script setup lang="ts">
import { useCounterStore } from '@/stores/counter'
const counterStore = useCounterStore()
</script>