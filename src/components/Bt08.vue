<template>
  <div>
    <button @click="handleIncrease">Tăng dần</button>
    <button @click="handleDecrease">Giảm dần</button>
    <p>{{ arr }}</p>
  </div>
</template>
<script setup>
import { ref } from "vue";

const arr = ref([5, 8, 2, 9, 4, 3]);
const handleIncrease = () => {
  arr.value.sort((a, b) => a - b);
};
const handleDecrease = () => {
  arr.value.sort((a, b) => b - a);
};
</script>
<style scoped></style>
