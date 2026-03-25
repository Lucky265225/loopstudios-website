<script setup>
import Creation from './components/Creation.vue';
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
  
  <div class="h-screen">

    <Navbar :menuItems="menuItems"/>
    <Creation/>

  </div>
  
</template>

<style scoped></style>
