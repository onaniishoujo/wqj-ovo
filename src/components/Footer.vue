<template>
    <footer class="mx-auto overflow-hidden w-full p-0 bg-gradient-to-l from-[#bd34fe] to-[#41d1ff]" id="jsi-flying-fish-container"></footer>
</template>

<script setup lang="ts">
import fish from '../assets/fish.js'
import { onMounted } from 'vue'

onMounted(() => {
    fish.init()
})
</script>