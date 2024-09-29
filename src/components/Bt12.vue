<template>
  <div>
    <div
      style="
        width: 200px;
        height: 50px;
        background-color: darkgoldenrod;
        display: flex;
        justify-content: center;
        align-items: center;
      "
      v-if="isNotificationShown"
    >
      Hiển thị nội dung ở đây
    </div>
    <br />

    <button
      style="color: black; background-color: dodgerblue"
      @click="toggleNotification"
    >
      {{ buttonText }}
    </button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const buttonText = "Show notification";
const isNotificationShown = ref(false);

const toggleNotification = () => {
  isNotificationShown.value = true;

  setTimeout(() => {
    isNotificationShown.value = false;
  }, 5000);
};
</script>
