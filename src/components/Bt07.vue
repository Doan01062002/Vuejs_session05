<template>
  <div>
    <button :class="activeIndex === 1 ? 'active' : ''" @click="handleButton1">
      button 1
    </button>
    <button :class="activeIndex === 2 ? 'active' : ''" @click="handleButton2">
      button 2
    </button>
    <button :class="activeIndex === 3 ? 'active' : ''" @click="handleButton3">
      button 3
    </button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const activeIndex = ref(1);
const handleButton1 = () => {
  activeIndex.value = 1;
};
const handleButton2 = () => {
  activeIndex.value = 2;
};
const handleButton3 = () => {
  activeIndex.value = 3;
};
</script>
<style scoped>
.active {
  background-color: red;
  color: white;
}
</style>
