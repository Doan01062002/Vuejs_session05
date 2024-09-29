<template>
  <div>
    <ul>
      <li v-if="userRole === 'admin'">Admin</li>
      <li v-if="userRole === 'user'">User</li>
      <li v-if="userRole === 'guest'">Guest</li>
    </ul>
  </div>
</template>
<script setup>
const userRole = "user";
</script>
<style scoped></style>
