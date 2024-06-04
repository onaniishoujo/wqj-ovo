<script setup lang="ts">
import Main from './components/Main.vue'
import Banner from './components/Banner.vue'
// import Content from './components/Content.vue'
import Navbar from './components/Navbar.vue'
import Sakana from './components/Sakana.vue'
</script>

<template>
  <Navbar></Navbar>
  <Banner></Banner>
  <Main></Main>
  <div class="absolute left-1/2 -translate-x-1/2" id="sakana-widget"></div>
  <Sakana></Sakana>
  <a id="content"></a>
  <!-- <Content>
    <template #title>杰哥为什么喜欢嫖娼</template>
    <template #text>因为杰哥是变态</template>
  </Content>
  <br>
  <Content>
    <template #title>Vue</template>
    <template #text>Vue3</template>
  </Content>
  <br>
  <Content>
    <template #title>Tailwind</template>
    <template #text>TailwindCSS</template>
  </Content> -->

</template>
