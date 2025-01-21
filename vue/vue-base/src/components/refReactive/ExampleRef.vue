<template>
  <div>
    <p>카운트: {{ count }}</p>
    <button @click="increment">카운트 증가</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';


const count = ref(0); // 숫자 값을 반응형으로 선언

const increment = () => {
  count.value++; // count의 값을 변경
};
</script>
