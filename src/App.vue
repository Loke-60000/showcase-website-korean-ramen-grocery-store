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

  body{
    width: 100vw;
    margin: 0;
    left: 0;
    overflow-x: hidden;
  }

</style>