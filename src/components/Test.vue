<script setup lang="ts">
const props = defineProps({
    message: String
})
</script>

<template>
    <div>{{props.message}}</div>
    <slot />
</template>