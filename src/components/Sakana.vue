<script setup lang="ts">
import 'sakana-widget/lib/index.css'
import SakanaWidget, { type SakanaWidgetCharacter } from 'sakana-widget'

const wqj = SakanaWidget.getCharacter('chisato') as SakanaWidgetCharacter
wqj.image = '/src/assets/sakana.webp'
SakanaWidget.registerCharacter('wqj', wqj)
new SakanaWidget({ character: 'wqj', size: 300}).mount('#sakana-widget')
</script>
