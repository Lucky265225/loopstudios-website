<script setup>

defineProps({
    menuItems : Array,
    icons : Array
})

</script>

<template>
  
    <section class="bg-black mt-20 py-10">
        <div class="md:w-full lg:w-[60%] m-auto flex flex-col items-center md:flex-row md:justify-between">
            <!-- logo + nav -->
            <div class=" flex flex-col space-y-3">
                <img src="../assets/logo.svg" alt="" class="w-fit m-auto mb-5 md:m-0">
                <div class="flex flex-col items-center md:flex-row md:items-start space-y-3 md:space-y-0 md:space-x-3">
                    <div v-for="item in menuItems" :key="item.name" class="group text-white">
                        <a :href="item.link">{{ item.name }}</a>
                        <div class="mx-2 group-hover:border-b group-hover:border-blue-50"></div>
                    </div>
                </div>
            </div>

            <!-- icon + desc -->
            <div class="flex flex-col items-center space-y-3 md:items-start mt-5 md:mt-0">
                <div class="flex space-x-3">
                    <div v-for="icon in icons">
                        <a href="">
                            <img :src="icon.path" alt="">
                        </a>
                    </div>
                </div>
                <p class="text-gray-500">@ 2022 Loopstudios All Rights Reserved</p>
            </div>
        </div>
    </section>
  
</template>

<style scoped></style>
