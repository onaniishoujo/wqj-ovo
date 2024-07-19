<template>
  <div class="typewriter-container">
    <div class="typewriter">
      <span>{{ typedText }}</span><span class="cursor" v-if="showCursor">|</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, watch, onMounted } from 'vue';

interface TypewriterProps {
  text: string;
  speed?: number;
  backSpeed?: number;
  cursor?: boolean;
  loop?: boolean;
  pause?: number;
}

const props = defineProps<TypewriterProps>();

const typedText = ref('');
const currentIndex = ref(0);
const showCursor = ref(props.cursor ?? true);

// let interval: NodeJS.Timeout | null = null;
let interval: any;

const startTyping = () => {
  clearInterval(interval as any); // NodeJS.Timeout);
  currentIndex.value = 0;
  interval = setInterval(() => {
    if (currentIndex.value <= props.text.length) {
      typedText.value = props.text.slice(0, currentIndex.value);
      currentIndex.value++;
    } else {
      clearInterval(interval as any); // NodeJS.Timeout);
      showCursor.value = false;
      if (props.loop) {
        restartTyping();
      }
    }
  }, props.speed ?? 100); // default speed: 100ms
};

const restartTyping = () => {
  clearInterval(interval as any); // NodeJS.Timeout);
  interval = setInterval(() => {
    if (currentIndex.value >= 0) {
      typedText.value = props.text.slice(0, currentIndex.value);
      currentIndex.value--;        
    } else {
      clearInterval(interval as any) // NodeJS.Timeout);
      setTimeout(() => {
        currentIndex.value = 0;
        typedText.value = '';
        showCursor.value = true;
        startTyping();
      }, props.pause ?? 1000); // pause 1 second before restarting
    }
  }, props.backSpeed ?? 100); // default speed: 100ms
};

onMounted(() => {
  startTyping();
});

watch(() => props.text, () => {
  typedText.value = '';
  currentIndex.value = 0;
  showCursor.value = true;
  startTyping();
});

</script>

<style scoped>
.typewriter-container {
  height: 200px; /* 固定高度容器 */
  overflow: visible; /* 内容溢出时隐藏 */
  /* border: 1px solid #ccc; /* 可选：添加边框 */ 
  padding: 10px; /* 可选：添加内边距 */
}

.typewriter {
  font-family: 'LXGW WenKai', sans-serif;
  /* font-family: 'Courier New', Courier, monospace; 可选：选择打字机风格的字体 */
  /* font-size: 18px; 可选：字体大小 */
  /* line-height: 24px; 可选：行高 */
  white-space: pre-wrap; /* 可选：保留换行符 */
}
.cursor {
  animation: blink-caret 0.75s step-end infinite;
}

@keyframes blink-caret {
  from, to { opacity: 1; }
  50% { opacity: 0; }
}
</style>
