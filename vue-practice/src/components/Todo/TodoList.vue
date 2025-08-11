<script setup lang="ts">

import TodoItem from './TodoItem.vue';


interface Todo {
  id:number;
  text:string;
  completed:boolean;
}

defineProps<{
  todos: Todo
}>()

</script>


<template>
  <ul class="todo-list">
    <TodoItem />
  </ul>
  <div class="empty-state">
    <p>할 일이 없습니다~  새로운 할 일을 추가해보세요.</p>
  </div>
</template>

<style scoped>

.todo-list{
  border: 1px solid #ddd;
  list-style: none;
  
}

.empty-state{
  padding: 40px;
  color: #888
}

</style>