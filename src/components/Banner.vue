<template>
    <!-- PC端容器 -->
    <div class="hidden lg:inline">

        <!-- 模糊遮罩 -->
        <div class="absolute bg-[#ffffff80] -z-10 backdrop-blur-2xl w-4/5 h-3/4 rounded-3xl left-0 right-0 m-auto top-0 bottom-0"></div>

        <!-- 标题 -->
        <div class="w-auto text-left mx-44 mt-32">
            <strong id="title" class="text-transparent text-9xl bg-gradient-to-tl from-[#bd34fe] to-[#41d1ff] bg-clip-text">杰哥嫖娼</strong>
            <p class="mt-10"><br>当你凝视杰哥时&nbsp;杰哥也在凝视你</p><br>
            <button @click="learnMore" class="text-white rounded-3xl text-2xl font-light border bg-gradient-to-tl from-[#bd34fe] to-[#47caff]">&nbsp;&nbsp;&nbsp;&nbsp;Learn More...&nbsp;&nbsp;&nbsp;&nbsp;</button>
        </div>
        <!-- 图片背景容器 -->
        <div class="flex justify-center items-center">
            <div id="image-bg" class="absolute w-[400px] h-[400px] aspect-square right-52 top-20 bg-cover">
        </div>
        <!-- 图片 -->
        <img src="../assets/wico.jpg" class="max-w-[320px] max-h-[320px] z-0 absolute top-[17rem] rounded-full outline-dashed outline-sky-100 right-20 transform -translate-x-1/2 -translate-y-1/2" />
        </div>
    </div>

    <!-- 移动端容器 -->
    <div class="lg:hidden inline">

        <!-- 模糊遮罩 -->
        <div class="absolute bg-[#ffffff80] -z-10 backdrop-blur-lg w-4/5 h-3/4 rounded-3xl left-0 right-0 m-auto top-0 bottom-0"></div>

        <!-- 图片背景容器 -->
        <div class="flex justify-center items-center">
            <div id="image-bg" class="absolute md:max-w-[392px] md:max-h-[392px] w-[256px] h-[256px] aspect-square top-24 bg-cover">
        </div>
        <!-- 图片 -->
        <img src="../assets/wico.jpg" class="md:max-w-[256px] md:max-h-[256px] max-w-[192px] max-h-[192px] absolute top-52 rounded-full outline-dashed outline-sky-100 transform -translate-x-1/2 -translate-y-1/2 aspect-square left-1/2" />
        </div>
        <!-- 标题 -->
        <div class="top-56 relative mx-10 mt-28 text-center">
            <strong id="title" class="text-transparent bg-gradient-to-tl from-[#bd34fe] to-[#41d1ff] bg-clip-text text-7xl">杰哥嫖娼</strong>
            <p><br>当你凝视杰哥时&nbsp;杰哥也在凝视你</p><br>
            <button @click="learnMore" class="text-white rounded-3xl text-2xl font-light border bg-gradient-to-tl from-[#bd34fe] to-[#47caff]">&nbsp;&nbsp;&nbsp;&nbsp;Learn More...&nbsp;&nbsp;&nbsp;&nbsp;</button>
        </div>
    </div>
</template>

<script setup lang="ts">
function learnMore():void {
    location.href.indexOf('#content') == -1 ? location.href += '#content' : location.reload()
}
</script>

<style>
/* @keyframes turnloop {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
  }
} */

#image-bg {
    background-image: linear-gradient(-45deg, #bd34fe 50%, #47caff 50%);
    border-radius: 50%;
    filter: blur(56px);
    /* animation: turnloop 10s linear infinite;
    -webkit-animation: turnloop 10s linear infinite; */
}

#title {
    font-family: 'LXGW WenKai';
}
</style>
