<script setup>
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
            <nav class="flex items-center justify-between font-bold text-white">
                <img src="../assets/logo.svg" alt="">
                <!-- desktop -->
                <div class="hidden h-10 font-sans md:flex md:space-x-8">
                    <div v-for="item in menuItems" :key="item.name" class="group">
                        <a :href="item.link">{{ item.name }}</a>
                        <div class="mx-2 group-hover:border-b group-hover:border-blue-50"></div>
                    </div>
                </div>
                <!-- mobile -->
                <img src="../assets/icon-hamburger.svg" alt="" class="md:hidden">
            </nav>
        </div>
    </section>
  
</template>

<style scoped></style>
