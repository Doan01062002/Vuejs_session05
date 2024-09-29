<template>
  <div>
    <p>Khi giá trị của: {{ isShow }}</p>
    <p v-show="isShow">Rikkei Academy</p>
    <button @click="handleClick">Hiện</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const isShow = ref(false);
const handleClick = () => {
  isShow.value = true;
};
</script>
<style scoped></style>
