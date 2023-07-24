<script setup lang="ts">
import { RouterLink } from 'vue-router'


</script>

<template>
    <nav>
    <v-btn value="home" block rounded="0" variant="tonal" @click=RouterLink to="/">
        Home
        <!-- <RouterLink to="/">Home</RouterLink> --> 
    </v-btn>
    <v-btn value="about" block rounded="0" variant="tonal" @click=RouterLink to="/about">
        About
        <!-- <RouterLink to="/about">About</RouterLink> -->
    </v-btn>
    </nav>

</template>
