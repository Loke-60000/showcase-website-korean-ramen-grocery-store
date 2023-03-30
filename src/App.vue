<script setup>
import MainNavbar from './components/MainNavbar.vue'
import MainFooter from './components/MainFooter.vue'

</script>

<template>
  <MainNavbar/>
  <nav>
    <!-- <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink> -->
  </nav>
  <RouterView />
  <MainFooter/>
</template>

<style>
  @import url(./assets/font/style.css);
  *{font-family: A-OTF Shin Go Pro R;}
</style>