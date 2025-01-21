<template>
  <div>
    <p>{{ user.name }} - 나이: {{ user.age }}</p>
    <button @click="updateAge">나이 증가</button>
  </div>
</template>


<script setup>
import { reactive } from 'vue';


const user = reactive({ name: '홍길동', age: 25 });

const updateAge = () => {
  user.age++; // 객체의 값을 변경
};


</script>
