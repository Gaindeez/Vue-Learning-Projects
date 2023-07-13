<script setup lang="ts">
//import HelloWorld from './components/HelloWorld.vue' 
import NavBar from './components/NavBar.vue';
</script>

<template>
  <div>
    <NavBar :items="[
      { label: 'Home', path: '/' },
      { label: 'About', path: '/about' },
      { label: 'Contact', path: '/contact' },
    ]" />
  </div>
  
  <!-- <HelloWorld msg="Vite + Vue" /> --> 
</template>

<style>

</style>
