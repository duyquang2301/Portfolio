<template>
  <div class="bg-[#fff] min-h-screen">
    <!-- Wrap components in Suspense to handle loading -->
     <Suspense>
      <template #default>
        <!-- Wrap all Components inside a single root element -->
         <div>
            <NavBar />
            <HeroSection />
            <ServiceSection />
            <AboutSection />
      </div>
    </template>
    <template #fallback>
      <div class="flex justify-center items-center min-h-screen">
          <loadingSpinner />
      </div>
    </template>
  </Suspense>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from "vue";
const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const HeroSection = defineAsyncComponent(()=>import('@/components/HeroSection.vue'));
const ServiceSection = defineAsyncComponent(()=>import('@/components/ServiceSection.vue'));
const AboutSection = defineAsyncComponent(()=>import('@/components/SchoolSection.vue'));
</script>
