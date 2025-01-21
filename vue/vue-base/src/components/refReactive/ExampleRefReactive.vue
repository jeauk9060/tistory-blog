<template>
  <div>
    <p>현재 값: {{ count }}</p>
    <button @click="increment">값 증가</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

const increment = () => {
  count.value++;
};


</script>
