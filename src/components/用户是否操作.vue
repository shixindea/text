<template>
  <div class='HelloWorld-container'>
  
  </div>
</template>
 
<script setup lang="ts">
import { onMounted } from 'vue'
import { useIdle } from '@vueuse/core'

const { idle, lastActive } = useIdle(5 *  1000) // 5 min

onMounted(() => {
  setInterval(() => {
  console.log(idle.value, lastActive.value)
}, 1000)
})

</script>
<style scoped></style>