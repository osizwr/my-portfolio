<template>
  <div class="bg-[#fafafa] min-h-screen">
    <Suspense>
      <template #default>
        <div>
          <NavBar/>
          <HeroSection/>
          <AboutSection/>
          <ServicesSection/>
          <ProjectSection/>
          <ContactSection/>
          <FooterSection/>
          <BackToTop/>
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
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
const FooterSection =defineAsyncComponent((  )=>import('@/components/FooterSection.vue'))
const BackToTop =defineAsyncComponent((  )=>import('@/components/BackToTop.vue'))
import LoadingSpinner from './components/LoadingSpinner.vue';
</script>