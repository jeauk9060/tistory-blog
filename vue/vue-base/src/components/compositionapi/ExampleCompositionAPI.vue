<template>
  <button @click="increment">숫자 세기: {{ count }}</button>
</template>

<script setup>
import { ref, onMounted } from 'vue'

// 반응형 상태
const count = ref(0)

// 상태를 변경하고 업데이트를 트리거하는 함수
function increment() {
  count.value++
}

// 생명주기 훅
onMounted(() => {
  console.log(`숫자를 세기 위한 초기값은 ${count.value} 입니다.`)
})
</script>

<style scoped></style>
