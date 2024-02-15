<template>
</template>
<script setup>
import { ref, onMounted } from 'vue';
import data from '../data.json';

const userId = ref(null);
const user = ref(null);

onMounted(() => {
  // Fetch user data based on userId
  const userObj = data.find(u => u.id === userId.value);
  if (userObj) {
    user.value = userObj;
  } else {
    // Handle the case where the user is not found
  }
});
</script>