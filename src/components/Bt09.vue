<template>
  <div>
    <h3>Gender: {{ renderGender }}</h3>
    <button @click="randomGender">Random gender</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const gender = ["Nam", "Nữ", "Khác"];
const renderGender = ref(gender[0]);

const randomGender = () => {
  renderGender.value = gender[Math.floor(Math.random() * gender.length)];
};
</script>
<style scoped></style>
