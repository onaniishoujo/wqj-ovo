<template>
    <!-- PC端容器 -->
    <div class="hidden lg:inline">
        <!-- 标题 -->
        <div class="w-auto text-left mx-44 mt-32">
            <strong id="title" class="text-transparent text-8xl bg-gradient-to-tl from-[#bd34fe] to-[#41d1ff] bg-clip-text">{{ wqjTitle }}</strong>
            <p v-html="wqjPhrase"></p><br>
            <button @click="learnMore" class="text-white rounded-3xl text-2xl font-light border bg-gradient-to-tl from-[#bd34fe] to-[#47caff]">&nbsp;&nbsp;&nbsp;&nbsp;Learn More...&nbsp;&nbsp;&nbsp;&nbsp;</button>
        </div>
        <!-- 图片背景容器 -->
        <div class="flex justify-center items-center">
            <div id="image-bg" class="absolute w-[320px] h-[320px] aspect-square right-60 top-24 bg-cover">
        </div>
        <!-- 图片 -->
        <img src="/src/assets/wqjh3.webp" class="z-0 absolute top-64 rounded-full outline-dashed outline-sky-100 right-52 transform -translate-x-1/2 -translate-y-1/2" />
        </div>
    </div>

    <!-- 移动端容器 -->
    <div class="lg:hidden inline">
        <!-- 图片背景容器 -->
        <div class="flex justify-center items-center">
            <div id="image-bg" class="absolute w-[256px] h-[256px] aspect-square top-24 bg-cover">
        </div>
        <!-- 图片 -->
        <img src="/src/assets/wqjh3.webp" class="max-w-[180px] max-h-[180px] absolute top-52 rounded-full outline-dashed outline-sky-100 transform -translate-x-1/2 -translate-y-1/2 aspect-square left-1/2" />
        </div>
        <!-- 标题 -->
        <div class="top-56 relative mx-10 mt-32 text-center">
            <strong id="title" class="text-transparent bg-gradient-to-tl from-[#bd34fe] to-[#41d1ff] bg-clip-text text-7xl">{{ wqjTitle }}</strong>
            <p v-html="wqjPhrase"></p><br>
            <button @click="learnMore" class="text-white rounded-3xl text-2xl font-light border bg-gradient-to-tl from-[#bd34fe] to-[#47caff]">&nbsp;&nbsp;&nbsp;&nbsp;Learn More...&nbsp;&nbsp;&nbsp;&nbsp;</button>
        </div>
    </div>
</template>

<script setup lang="ts">
let wqjTitle:string = '杰哥嫖娼'
let wqjPhrase:string = '<br>当你凝视杰哥时&nbsp;杰哥也在凝视你'
function learnMore():void {
    location.href.indexOf('#content') == -1 ? location.href += '#content' : location.reload()
}
</script>

<style>
@font-face {
    font-family: 'LXGW WenKai';
    src: url('/src/assets/font.woff2');
}

@keyframes turnloop {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
  }
}

#image-bg {
    background-image: linear-gradient(-45deg, #bd34fe 50%, #47caff 50%);
    border-radius: 50%;
    filter: blur(56px);
    animation: turnloop 10s linear infinite;
}

#title {
    font-family: 'LXGW WenKai';
}
</style>
