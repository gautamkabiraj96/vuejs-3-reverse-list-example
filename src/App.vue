<script setup>
import { ref, computed } from 'vue'

const myList = ref([
  'Apple', 'Banana', 'Mango', 'Pineapple', 'Grapes'
])

const reversedList = computed(() => {
  return myList.value.slice().reverse()
})
</script>

<template>
<div>
    <p>
      <ul>
        <li v-for="(item, i) in reversedList" :key="i">
          {{item}}
        </li>
      </ul>
    </p>
</div>
</template>

<style scoped>
</style>
