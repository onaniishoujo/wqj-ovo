<template>
    <nav :class="{ 'bg-transparent backdrop-blur-3xl border-b-0': isTop, 'bg-white shadow-md border-b': !isTop }" class="z-50 w-full h-[64px] border flex lg:fixed top-0 items-center ease-in-out delay-150">
        <span id="logo" class="inline-block ml-10 outline-dashed rounded outline-1 outline-offset-8 outline-gray-200 text-lg"><a href="/">杰哥嫖娼</a></span>
        <img @click="avatarLink" class="hover:outline-offset-4 hover:outline-dashed outline-1 outline-gray-400 inline-block absolute right-10 h-[64px] rounded-full ring-2 ring-[#47caff] shadow-2xl" alt="avatar" src="/src/assets/avatar.jpg"/>
    </nav>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isTop = ref(true);

const handleScroll = () => {
    isTop.value = window.scrollY === 0;
}

function avatarLink():void {
    location.href = 'https://shoujo.deno.dev/'
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
})
</script>

<style>
#logo {
    font-family: 'LXGW WenKai';
}
</style>
