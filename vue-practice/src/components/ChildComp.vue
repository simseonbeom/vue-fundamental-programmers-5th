

<script setup lang="ts">


const props = defineProps<{
  score: number,
  comment: string
}>()


</script>

<template>
  <div>
    <input 
      type="range" 
      min="0" 
      max="5"
    >
    
    <textarea

    ></textarea>

  </div>
</template>

<style scoped>

</style>