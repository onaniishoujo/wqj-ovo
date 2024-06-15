<template>
    <canvas ref="bgCanvas" class="absolute top-0 h-dvh w-dvw -z-50"></canvas>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue'
import webGLFluidEnhanced from 'webgl-fluid-enhanced'

const bgCanvas = ref<HTMLCanvasElement | null>(null)
onMounted(() => {
    if (bgCanvas.value){
        webGLFluidEnhanced.simulation(bgCanvas.value, {BACK_COLOR: '#ffffff', DYE_RESOLUTION: 512})
        setInterval(()=>{
            webGLFluidEnhanced.splats()
        }, 3000)
    }
})
</script>