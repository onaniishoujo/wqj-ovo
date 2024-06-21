<template>
    <h1 class="mx-auto w-4/5 drop-shadow-2xl text-6xl sm:text-8xl font-extrabold lg:text-left text-center mb-28">「杰哥」是什么? <span class="hidden lg:inline text-xl mx-auto ml-10 text-gray-600">ブラザージャーとは? </span></h1>
    <div class="lg:hidden text-xl text-center mx-auto text-gray-600 font-extrabold w-4/5 -mt-20 mb-5">ブラザージャーとは? </div>
    <div class="card mx-auto w-4/5 bg-gray-100 shadow-lg">
        <div class="card-body">
            <Sakana />
        </div>
    </div>
    <Chat />
    <Card />
    <Part />
</template>

<script setup lang="ts">
import Sakana from './Sakana.vue'
import Chat from './Chat.vue'
import Card from './Card.vue'
import Part from './Part.vue'
</script>
