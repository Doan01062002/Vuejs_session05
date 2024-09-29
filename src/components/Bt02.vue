<template>
  <div>
    <p>Khi giá trị của: {{ isShow }}</p>
    <button @click="handleClick">{{ isShow === false ? "Hiện" : "Ẩn" }}</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const isShow = ref(false);
const handleClick = () => {
  isShow.value = !isShow.value;
};
</script>
<style scoped></style>
