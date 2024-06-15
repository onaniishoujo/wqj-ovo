<template>
    <div class="absolute left-1/2 -translate-x-1/2" ref="sakana_widget"></div>
    <br><br><br><br><br><br><br><br><br><br>
</template>

<script setup lang="ts">
import 'sakana-widget/lib/index.css'
import SakanaWidget, { type SakanaWidgetCharacter } from 'sakana-widget'
import { ref, onMounted } from 'vue'

const sakana_widget = ref<HTMLElement | null>(null)

onMounted(()=>{
    if (sakana_widget.value){
        const wqj = SakanaWidget.getCharacter('chisato') as SakanaWidgetCharacter
        wqj.image = '/src/assets/sakana.webp'
        SakanaWidget.registerCharacter('wqj', wqj)
        new SakanaWidget({ character: 'wqj', size: 300}).mount(sakana_widget.value)
    }
})
</script>
