<script setup lang="ts">
import { onUnmounted, ref } from "vue";
import Test from "./components/Test.vue"

const counter = ref(0)

const interval = setInterval(() => {
  counter.value++
}, 500)

onUnmounted(() => {
  clearInterval(interval)
})

</script>

<template>
<Test :message="'hello ' + counter">
  <Test :message="'world ' + counter" />
</Test>
</template>