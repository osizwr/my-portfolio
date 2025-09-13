<template>
  <div class="bg-[#fafafa] min-h-screen">
    <NavBar/>
    <HeroSection/>
    <AboutSection/>
    <ServicesSection/>
    <ProjectSection/>
    <ContactSection/>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';

const NavBar =defineAsyncComponent((  )=>import('@/components/NavBar.vue'))
const HeroSection =defineAsyncComponent((  )=>import('@/components/HeroSection.vue'))
const AboutSection =defineAsyncComponent((  )=>import('@/components/AboutSection.vue'))
const ServicesSection =defineAsyncComponent((  )=>import('@/components/ServicesSection.vue'))
const ProjectSection =defineAsyncComponent((  )=>import('@/components/ProjectSection.vue'))
const ContactSection =defineAsyncComponent((  )=>import('@/components/ContactSection.vue'))
</script>