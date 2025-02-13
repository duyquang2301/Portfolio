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
            <ExperienceSection />
            <ProjectSection />

            <Footer />
            <BackToTop />
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
const ExperienceSection = defineAsyncComponent(()=>import('@/components/ExperienceSection.vue'));
const ProjectSection = defineAsyncComponent(()=>import('@/components/ProjectSection.vue'));


const Footer = defineAsyncComponent(()=>import('@/components/Footer.vue'));
const BackToTop = defineAsyncComponent(()=>import('@/components/BackToTop.vue'));
</script>
