<script setup lang="ts">
import { useCounterStore } from "@/stores/counter";

const store = useCounterStore();
</script>

<template>
  <main>Hello world</main>
  <div>Count: {{ store.count }}</div>
  <div>Double count: {{ store.doubleCount }}</div>
  <div>
    <button @click="store.increment">Increment</button>
  </div>
</template>
