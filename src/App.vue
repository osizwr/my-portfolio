<template>
  <div class="bg-[#fafafa] min-h-screen">
    <NavBar/>
    <HeroSection/>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';

const NavBar =defineAsyncComponent((  )=>import('@/components/NavBar.vue'))
const HeroSection =defineAsyncComponent((  )=>import('@/components/HeroSection.vue'))
</script>