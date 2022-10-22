<script setup lang="ts">
import { storeToRefs } from "pinia";
import { useCounterStore } from "@/stores/counter";

const store = useCounterStore();

// we cannot destructure reactive properties from store object directly
// without losing reactivity, that's why we need to use storeToRefs
const { count, doubleCount } = storeToRefs(store);

// actions can just be extracted
const { increment } = store;
</script>

<template>
  <main>Hello world</main>
  <div>Count: {{ count }}</div>
  <div>Double count: {{ doubleCount }}</div>
  <div>
    <button @click="increment">Increment</button>
  </div>
</template>
