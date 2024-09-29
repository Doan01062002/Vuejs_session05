<template>
  <div>
    <button @click="handleRandom">Random number</button>
    <p>{{ arr }}</p>
  </div>
</template>
<script setup>
import { ref } from "vue";

const arr = ref([]);
const handleRandom = () => {
  arr.value.push(Math.floor(Math.random() * 10));
};
</script>
<style scoped></style>
