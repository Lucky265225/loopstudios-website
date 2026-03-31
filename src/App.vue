<script setup>
import Creation from './components/Creation.vue';
import Feature from './components/Feature.vue';
import Navbar from './components/Navbar.vue';
import { ref } from 'vue'

// Menu: About, Careers, Events, Products, Supports
const menuItems = ref([
  {name:"About", link:"#"},
  {name:"Careers", link:"#"},
  {name:"Events", link:"#"},
  {name:"Products", link:"#"},
  {name:"Supports", link:"#"}
])

</script>

<template>
  
  <div class="h-screen flex flex-col space-y-20">

    <Navbar :menuItems="menuItems"/>

    <Feature/>

    <Creation/>

  </div>
  
</template>

<style scoped></style>
