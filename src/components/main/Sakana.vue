<template>
    <div class="flex flex-col lg:flex-row lg:items-end overflow-x-clip">
        <div data-aos="zoom-in" ref="sakana_widget" class="w-full sm:w-auto lg:order-1 mx-auto bg-white rounded-3xl shadow-xl"></div>
        <div class="lg:order-2 lg:w-1/2 p-2 lg:-translate-x-1/4 lg:ml-24">
            <span class="neon text-6xl translate-y-10 left-0 right-0 m-0 lg:left-auto lg:right-auto mx-10 lg:mx-0 blur-[24px]" style="position: absolute;">{{ koto }}</span>
            <span class="relative neon text-6xl lg:float-start my-10">{{ koto }}</span>
            <img data-aos="fade-left" class="rounded-3xl relative shadow-xl" src="/src/assets/laolai.png" alt="laolai" />
        </div>
    </div>
</template>

<script setup lang="ts">
import 'sakana-widget/lib/index.css'
import SakanaWidget, { type SakanaWidgetCharacter } from 'sakana-widget'
import { ref, onMounted } from 'vue'

const sakana_widget = ref<HTMLElement | null>(null)
const sound = new Audio('/sound.mp3')
const koto = ref('王庆杰 (老赖)')

function playEvent(): void {
    koto.value = '杰哥射了'
    sound.play()
    sound.loop = false
    sound.onended = () => { koto.value = '王庆杰 (老赖)' }
}

onMounted(()=>{
    if (sakana_widget.value){
        const wqj = SakanaWidget.getCharacter('chisato') as SakanaWidgetCharacter
        wqj.image = '/sakana.webp'
        SakanaWidget.registerCharacter('wqj', wqj)
        new SakanaWidget({ character: 'wqj', size: 300}).mount(sakana_widget.value)

        const widget_img = document.querySelector('.sakana-widget-img')
        widget_img?.addEventListener('click', playEvent)
        widget_img?.addEventListener('touchstart', playEvent)
    }
})
</script>

<style>
.neon {
    background-clip: text;
    background-image: linear-gradient(90deg, oklch(0.6971 0.329 342.55)4%, oklch(0.70735 0.275 2.36499) 22%, oklch(0.4912 0.3096 275.75) 45%, oklch(0.6294 0.2468 229.68) 67%, oklch(0.7676 0.184 183.61) 100.2%);
    border-bottom-color: rgb(229, 231, 235);
    border-bottom-style: solid;
    border-bottom-width: 0px;
    border-left-color: rgb(229, 231, 235);
    border-left-style: solid;
    border-left-width: 0px;
    border-right-color: rgb(229, 231, 235);
    border-right-style: solid;
    border-right-width: 0px;
    border-top-color: rgb(229, 231, 235);
    border-top-style: solid;
    border-top-width: 0px;
    box-sizing: border-box;
    color: oklch(0.278078 0.029596 256.848);
    color-scheme: light;
    display: block;
    /* font-family: Figtree, "Noto: Sans: JP", "Noto: Sans", Vazirmatn, sans-serif; */
    font-feature-settings: normal;
    /* font-size: 46.2px; */
    font-variation-settings: normal;
    font-weight: 900;
    /* height: 50.8125px; */
    /* line-height: 50.82px; */
    position: relative;
    scrollbar-color: oklch(0.278078 0.029596 256.848) rgba(0, 0, 0, 0);
    tab-size: 4;
    text-align: center;
    text-size-adjust: 100%;
    /* width: 138.609px; */
    word-break: auto-phrase;
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    -webkit-text-fill-color: rgba(0, 0, 0, 0);
}
.neon-back {
    background-clip: text;
    background-image: linear-gradient(90deg, oklch(0.6971 0.329 342.55) 4%, oklch(0.70735 0.275 2.36499) 22%, oklch(0.4912 0.3096 275.75) 45%, oklch(0.6294 0.2468 229.68) 67%, oklch(0.7676 0.184 183.61) 100.2%);
    border-bottom-color: rgb(229, 231, 235);
    border-bottom-style: solid;
    border-bottom-width: 0px;
    border-left-color: rgb(229, 231, 235);
    border-left-style: solid;
    border-left-width: 0px;
    border-right-color: rgb(229, 231, 235);
    border-right-style: solid;
    border-right-width: 0px;
    border-top-color: rgb(229, 231, 235);
    border-top-style: solid;
    border-top-width: 0px;
    box-sizing: border-box;
    color: oklch(0.278078 0.029596 256.848);
    color-scheme: light;
    display: block;
    filter: blur(24px);
    font-family: Figtree, "Noto Sans JP", "Noto Sans", Vazirmatn, sans-serif;
    font-feature-settings: normal;
    font-size: 46.2px;
    font-variation-settings: normal;
    font-weight: 900;
    grid-column-start: 1;
    grid-row-start: 1;
    height: 50.8125px;
    line-height: 50.82px;
    pointer-events: none;
    scrollbar-color: oklch(0.278078 0.029596 256.848) rgba(0, 0, 0, 0);
    tab-size: 4;
    text-align: center;
    text-size-adjust: 100%;
    transform: matrix(1, 0, 0, 1, 0, 0);
    width: 138.609px;
    word-break: auto-phrase;
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    -webkit-text-fill-color: rgba(0, 0, 0, 0);
}
</style>
