<template>
  <div>
    <p>Khi giá trị của biến isVisible = {{ isVisible }}</p>
    <button @click="handleClickShow">Hiển thị</button>
    <button @click="handleClickHide">Ẩn</button>
    <p v-show="isVisible">Welcom to Rikkei Education</p>
  </div>
</template>
<script setup>
import { ref } from "vue";

const isVisible = ref(false);
const handleClickShow = () => {
  isVisible.value = true;
};
const handleClickHide = () => {
  isVisible.value = false;
};
</script>
<style></style>
