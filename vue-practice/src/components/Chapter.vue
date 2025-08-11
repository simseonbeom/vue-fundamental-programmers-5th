


<script setup lang="ts">

import { provide, ref } from 'vue';
import ChildComp from './ChildComp.vue';
import { scoreKey } from '../store/score';


const score = ref(3);
const comment = ref('');

const updateScore = (v:number) => {
  score.value = v;
}

const updateComment = (v:string) => {
  comment.value = v;
}

provide(scoreKey,{score,comment,updateScore,updateComment});


</script>

<template>
  
  <ChildComp />
  <p>score : {{ score }}</p>
  <p>comment : {{ comment }}</p>

</template>

<style scoped>

</style>