<!-- 

vue의 리스트 렌더링은 v-for 디렉티브를 사용하여 만들 수 있습니다.


-->

<script setup lang="ts">
import { ref } from 'vue';


let id = 0;
// for(const a of arr ){

// }

const todos = ref([
  {id:id++, text:'HTML 배우기'},
  {id:id++, text:'CSS 배우기'},
  {id:id++, text:'JavaScript 배우기'},
  {id:id++, text:'Vue 배우기'},
])

</script>

<template>
  
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
      <button type="button">❌</button>
    </li>
  </ul>

</template>

<style scoped>

ul{
  li{
    margin-bottom: 1rem;
  }
}

button{
  margin-left: 2rem;
}

</style>