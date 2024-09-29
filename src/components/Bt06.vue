<template>
  <div>
    <p>Các số lẻ từ mảng:</p>
    <b v-for="number in arr">
      {{ number % 2 !== 0 ? number : " " }}
    </b>
  </div>
</template>
<script setup>
const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
</script>
<style></style>
