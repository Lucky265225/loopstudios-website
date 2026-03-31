<script setup>
import Creation from './components/Creation.vue';
import Feature from './components/Feature.vue';
import Footer from './components/Footer.vue';
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

const cards = ref([
  {title:"deep earth", desktop:"./src/assets/desktop/image-deep-earth.jpg", mobile:"./src/assets/mobile/image-deep-earth.jpg"},
  {title:"night arcade", desktop:"./src/assets/desktop/image-night-arcade.jpg", mobile:"./src/assets/mobile/image-night-arcade.jpg"},
  {title:"soccer team vr", desktop:"./src/assets/desktop/image-soccer-team.jpg", mobile:"./src/assets/mobile/image-soccer-team.jpg"},
  {title:"the grid", desktop:"./src/assets/desktop/image-grid.jpg", mobile:"./src/assets/mobile/image-grid.jpg"},
  {title:"from up above vr", desktop:"./src/assets/desktop/image-from-above.jpg", mobile:"./src/assets/mobile/image-from-above.jpg"},
  {title:"pocket borealis", desktop:"./src/assets/desktop/image-pocket-borealis.jpg", mobile:"./src/assets/mobile/image-pocket-borealis.jpg"},
  {title:"the curiosity", desktop:"./src/assets/desktop/image-curiosity.jpg", mobile:"./src/assets/mobile/image-curiosity.jpg"},
  {title:"make it fisheye", desktop:"./src/assets/desktop/image-fisheye.jpg", mobile:"./src/assets/mobile/image-fisheye.jpg"},
])

const icons = ref([
  {name:"facebook",path:"./src/assets/Assets/icon-facebook.svg"},
  {name:"twitter",path:"./src/assets/Assets/icon-twitter.svg"},
  {name:"pinterest",path:"./src/assets/Assets/icon-pinterest.svg"},
  {name:"instagram",path:"./src/assets/Assets/icon-instagram.svg"},
])

</script>

<template>
  
  <div class="h-screen flex flex-col space-y-20">

    <Navbar :menuItems="menuItems"/>

    <Feature/>

    <Creation :cards="cards"/>

    <Footer :menuItems="menuItems" :icons="icons"/>

  </div>
  
</template>

<style scoped></style>
