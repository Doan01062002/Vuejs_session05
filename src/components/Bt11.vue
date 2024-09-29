<template>
  <div>
    <h3>Danh sách User</h3>
    <input v-model="inputText" type="text" />
    <button @click="handleSearch">Tìm Kiếm</button>
    <ul>
      <li v-for="user in filterUser">{{ user }}</li>
    </ul>
  </div>
</template>
<script setup>
import { ref } from "vue";

const inputText = defineModel();

const filterUser = ref([]);
const users = [
  {
    id: 1,
    name: "Hạnh",
  },
  {
    id: 2,
    name: "Đoan",
  },
  {
    id: 3,
    name: "Phúc",
  },
  {
    id: 4,
    name: "Trúc",
  },
];

const handleSearch = () => {
  console.log(inputText.value);
  filterUser.value.push(users.filter((user) => user.name === inputText.value));
};
</script>
<style scoped></style>
