<script setup lang="ts">
import Banner from './components/Banner.vue'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import Main from './components/main/Main.vue'
import Comment from './components/Comment.vue'
import Company from './components/company/Company.vue'
import aos from 'aos'
import 'aos/dist/aos.css'

aos.init()
document.addEventListener('DOMContentLoaded', ()=>{
    const params = new URLSearchParams(location.search)
    const qname = params.get('name')?.replace(/<|>/g, '')
    if (qname) {
        document.documentElement.innerHTML = document.documentElement.innerHTML.replace(/王庆杰|杰哥/g, qname)
    }
})
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