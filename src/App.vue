<template>
  <div class="bg-[#fff] min-h-screen">
    <NavBar />
    <HeroSection/>
    <ServiceSection/>
    <AboutSection/>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from "vue";
const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const HeroSection = defineAsyncComponent(()=>import('@/components/HeroSection.vue'));
const ServiceSection = defineAsyncComponent(()=>import('@/components/ServiceSection.vue'));
const AboutSection = defineAsyncComponent(()=>import('@/components/SchoolSection.vue'));
</script>
