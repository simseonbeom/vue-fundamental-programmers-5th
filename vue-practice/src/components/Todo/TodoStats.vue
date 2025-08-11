<script setup lang="ts">
import { computed } from 'vue';



const props = defineProps<{
  total:number;
  completed:number;
}>()


// 파생 상태  완료되지 않은 할 일 갯수
const remainder = computed(()=> props.total - props.completed)

</script>

<template>
  <div class="stats">
    전체 : {{ total }} | 완료 : {{ completed }} | 남은 할 일 : {{ remainder }}
  </div>
</template>

<style scoped>

.stats{
  margin-bottom: 1rem;
  padding: 1rem;
  background-color: #a2a2a2;
  color:black;
  border-radius: 4px;
  font-weight: bold;
}

</style>