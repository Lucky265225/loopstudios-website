<script setup>
import { ref } from 'vue'

const hamburger = ref(false)

defineProps({
    menuItems: {
        type: Array,
        required: true
    }
})
</script>

<template>
  
    <section class="bg-[url(assets/mobile/image-hero.jpg)] bg-no-repeat bg-cover 
    md:bg-[url(assets/desktop/image-hero.jpg)]">
        <div class="container max-w-6xl mx-auto px-6 py-12">
            <nav class="flex items-center justify-between font-bold text-white mb-20">
                <img src="../assets/logo.svg" alt="" @click="">
                <!-- desktop -->
                <div class="hidden h-10 font-sans md:flex md:space-x-8">
                    <div v-for="item in menuItems" :key="item.name" class="group">
                        <a :href="item.link">{{ item.name }}</a>
                        <div class="mx-2 group-hover:border-b group-hover:border-blue-50"></div>
                    </div>
                </div>
                <!-- mobile -->
                <img src="../assets/icon-hamburger.svg" alt="" class="md:hidden" @click="hamburger = !hamburger">
                <!-- hamburger -->
                <div class="fixed top-0 right-0 w-full h-screen md:hidden bg-black text-white flex flex-col items-center p-5 space-y-4
                transform transition-transform duration-300" :class="hamburger ? 'translate-x-0' : 'translate-x-full'">
                    <img src="../assets/icon-close.svg" alt="" class="ml-auto" @click="hamburger = !hamburger">
                    <a v-for="item in menuItems" :href="item.link">{{ item.name }}</a>
                </div>
            </nav>

            <!-- box content -->
            <div class="w-fit tracking-widest text-white text-4xl font-thin border border-white p-5 mb-20">
                <h1>IMPRESSIVE</h1>
                <h1>EXPERIENCES</h1>
                <h1>THAT DELIVER</h1>
            </div>
        </div>
    </section>
  
</template>

<style scoped></style>
