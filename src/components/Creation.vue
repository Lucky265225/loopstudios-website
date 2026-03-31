<script setup>

defineProps({
    cards: Array
})

</script>

<template>
  
    <section class="md:w-full lg:w-[60%] m-auto">
        <!-- head -->
        <div class="flex justify-center md:justify-between mb-20">
            <h1 class="uppercase text-4xl font-thin">our creations</h1>
            <button class="btn hidden md:block">see all</button>
        </div>

        <!-- all cards -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-5">
            <div v-for="card in cards"
            class="relative md:h-96">
                <img :src="card.desktop" alt="" class="h-full hidden md:block">
                <img :src="card.mobile" alt="" class="w-full block md:hidden">
                <h3 class="absolute bottom-0 text-2xl text-white font-thin uppercase p-10 break-word">
                    {{ card.title }}
                </h3>
            </div>
            <button class="w-full btn block md:hidden">see all</button>
        </div>
    </section>
  
</template>

<style scoped></style>
