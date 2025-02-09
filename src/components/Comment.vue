<template>
    <h1 id="comh" class="w-5/6 mx-auto text-center font-bold text-4xl lg:text-6xl my-12 lg:indent-16">杰哥的评论区! </h1>
    <p class="w-5/6 mx-auto text-center"><del>反正就是评论区了 剩下的懒得写了</del></p>
    <div class="w-5/6 mx-auto mb-16">
        <div class="card lg:card-side bg-base-100 shadow-xl">
        <figure data-aos="zoom-in">
            <img src="/src/assets/mkas.webp" class="h-80 rounded-3xl sm:rounded shadow" alt="Album" />
        </figure>
        <div class="card-body">
            <h2 class="card-title">Douglas MacArthur 麦克阿瑟曾说过</h2>
            <div class="chat chat-start">
            <div data-aos="zoom-in-right" class="chat-bubble text-xl lg:text-6xl text-white left-0 right-0 m-auto lg:translate-y-1/2 bg-[#66ccff]">
                &nbsp;我喜欢<strong>于明月</strong>!&nbsp;<br>
                (I like Ding Mingyue!)
            </div>
            </div>
            <div class="card-actions justify-end">
            </div>
        </div>
        </div>

        <div class="hero bg-base-200 min-h-full rounded-box mt-10">
        <div class="hero-content flex-col lg:flex-row-reverse">
            <img data-aos="zoom-in" src="../assets/zzx.webp" class="max-w-sm rounded-lg shadow-2xl" />
            <div>
            <h1 class="text-5xl font-bold">Spider-Man曾说过</h1>
            <div data-aos="zoom-in-right" class="chat chat-start">
            <p class="py-6 chat-bubble text-xl lg:text-6xl text-white">
                我也喜欢<strong>于明月</strong>! <br>
                (I also like Ding Mingyue! )
            </p></div>
            </div>
        </div>
        </div>

        <div class="card lg:card-side bg-base-100 shadow-xl mt-10">
        <figure data-aos="zoom-in">
            <img src="/src/assets/wico.jpg" class="h-80 rounded-3xl sm:rounded shadow" alt="Album" />
        </figure>
        <div class="card-body">
            <h2 class="card-title">Wang Qingjie 木下加四点曾说过</h2>
            <span class="hidden lg:inline">( 脑子被边框夹了 )</span>
            <div class="chat chat-start">
            <div data-aos="zoom-in-right" class="chat-bubble text-xl lg:text-4xl lg:translate-y-1/4 text-white left-0 right-0 m-auto bg-[#66ccff]">
                你们都不是真爱!
                只有我喜欢<strong>丁明月</strong>!<br>
                (あなたがたの誰一人として真実の愛ではない! ディン・ミンユエが好きなのは私だけ!)
            </div>
            </div>
            <div class="card-actions justify-end">
            </div>
        </div>
        </div>

        <Waline :serverURL="serverURL" :path="path" :reaction="true" :requiredMeta="['nick']" :login="'disable'" />
    </div>
</template>

<script setup lang="ts">
import { Waline } from '@waline/client/component'
import '@waline/client/style'
  
const serverURL: string = 'https://pink.deno.dev/'
const path: string = location.pathname
</script>

<script lang="ts">
document.addEventListener('DOMContentLoaded', () => {
    document.getElementsByClassName('wl-reaction-title')[0].innerHTML = '你认为杰哥怎么样?'
})

function changeAvatar(): void {
    // 创建一个 MutationObserver 实例
    const observer = new MutationObserver((mutationsList, observer) => {
        for (const mutation of mutationsList) {
            // 检查是否有新节点被添加到 DOM 中
            if (mutation.type === 'childList') {
                const imgElement = document.querySelector('img.wl-user-avatar') as HTMLImageElement | null;
                if (imgElement) {
                    imgElement.src = '/nxavatar.jpg';
                    // 停止观察，因为已经找到了目标元素
                    observer.disconnect();
                    break;
                }
            }
        }
    });

    // 配置并开始观察整个文档的子节点变化
    observer.observe(document.documentElement, {
        childList: true, // 监听子节点的变化
        subtree: true,   // 在整个子树内观察变化
    });

    // 可选：如果超过一定时间还未找到目标元素，则停止观察
    setTimeout(() => {
        observer.disconnect();
        console.log('Observer disconnected.');
    }, 10000); // 设置一个适当的超时时间，例如 10 秒
}


changeAvatar()
</script>

<style>
:root {
    --waline-theme-color: #66ccff !important;
    --waline-active-color: #39c5bb !important;
}
#comh {
    font-family: 'LXGW Wenkai';
}
</style>