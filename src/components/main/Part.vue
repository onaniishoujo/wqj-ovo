<template>
    <div class="mx-auto w-5/6 drop-shadow-2xl text-6xl sm:text-8xl font-extrabold lg:text-left text-center mt-64 mb-96 lg:mb-0 lg:mt-40 translate-y-full lg:translate-y-0">
        <!-- translate-y-full lg:translate-y-0 -->
        <Typed :speed="250" :back-speed="60" cursor loop text="「杰哥」是变态。      " />
        <Typed :speed="250" :back-speed="60" cursor loop text="「杰哥」喜欢嫖娼。      " /></div>
    <div class="sm:hidden h-px sm:h-auto translate-y-full"></div>
</template>

<script setup lang="ts">
import Typed from '@/components/utils/Typed.vue'
</script>
