<template>
  <div class='HelloWorld-container'>
    <h2 v-for="item in data " :key="item">
      {{ item }}
    </h2>
  </div>
</template>
 
<script setup lang="ts">
import { ref } from 'vue';
const data = ref([1, 2, 3, 4, 5, 6, 7, 8])


</script>
<style scoped></style>