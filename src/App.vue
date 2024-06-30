<script setup lang="ts">
import Banner from './components/Banner.vue'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import Main from './components/main/Main.vue'
import Comment from './components/Comment.vue'
import Company from './components/company/Company.vue'
</script>

<template>
  <Navbar />
  <Banner /><br><br><br><br><br><br><br></br><br><br><br><br>
  <a id="content"></a>
  <Main />
  <Company />
  <Comment />
  <Footer />
</template>
