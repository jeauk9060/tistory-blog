<template>
  <div id="app">
    <!-- 데이터 바인딩 -->
    <h1>{{ title }}</h1>
    <!-- 조건부 렌더링 -->
    <p v-if="isVisible">이 문장은 조건부로 표시됩니다!</p>
    <!-- 반복 렌더링 -->
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ index + 1 }}. {{ item }}
      </li>
    </ul>
    <!-- 이벤트 바인딩 -->
    <button @click="handleClick">버튼 클릭!</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// 반응형 데이터
const title = ref("Vue 템플릿 예제");
const isVisible = ref(true);
const items = ref(["사과", "바나나", "체리"]);

// 메서드 정의
const handleClick = () => {
  alert("버튼을 클릭했습니다!");
};
</script>
