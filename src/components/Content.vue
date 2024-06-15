<template>
    <div class="mx-auto max-w-6xl rounded overflow-hidden shadow-lg">
    <div class="flex">
        <img class="aspect-square" :src="imgPath()" alt="wqj">
        <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2"><slot name="title"></slot></div>
        <p class="text-gray-700 text-base blur-sm hover:blur-none"><slot name="text"></slot></p>
        </div>
    </div>
    </div>
</template>
<script setup lang="ts">
function imgPath():string {
    const m: number = Math.random()
    if (m < 0.3333) {
        return '/src/assets/wqjh1.webp'
    } else if (m >= 0.3333 && m < 0.6666) {
        return '/src/assets/wqjh2.webp'
    } else {
        return '/src/assets/wqjh3.webp'
    }
}
</script>
