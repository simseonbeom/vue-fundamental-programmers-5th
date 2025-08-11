<script setup lang="ts">
import { ref } from 'vue';



const todos = ref([
  { id: 1, text: 'Vue 학습하기', completed: false},
  { id: 2, text: '컴포넌트 분리하기', completed: true},
  { id: 3, text: 'emit 이해하기', completed: false},
]);




</script>

<template>
  <div class="todo-app">
    <h1>할 일 목록</h1>

    <!--TodoList 컴포넌트를 사용해서 todos 데이터 리스트 렌더링 -->
    <TodoList/>
    
  </div>
</template>

<style scoped>


.todo-app {
  max-width: 600px;
  /* margin-top: 0 auto; */
  padding: 20px;
  border: 1px solid #fff;
  border-radius: 1rem;
}


</style>