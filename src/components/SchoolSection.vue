<template>
    <section class="text-[#868e96] mt-18" id="education">
      <!-- Background Blur Effect -->
      <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
        <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"></div>
      </div>
  
      <!-- Education Content -->
      <div class="md:grid gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
        <div data-aos="fade-up">
          <h2 class="text-4xl font-bold text-[#868e96] text-left mb-8"
              :style="{ fontFamily: 'Grechen Fuemen, sans-serif' }">
            Education
          </h2>
        </div>
  
        <!-- Right Column: Education Details -->
        <div data-aos="fade-up" class="flex items-start space-x-6">
          <!-- University Logo -->
          <img src="@/assets/bk.png" alt="University Logo"
               class="w-40 h-40 shadow-lg">
          <!-- Education Information -->
          <div class="px-4 gap-8">
            <h3 class="text-2xl font-semibold text-black">
              Da Nang University of Science and Technology
            </h3>
            <p class="text-lg font-medium text-[#868e96]">
              Information Technology Industry
            </p>
            <p class="text-sm text-[#868e96]">
              2020 - Present
            </p>
            <p class="text-sm text-[#868e96]">
              GPA - 3.32
            </p>
            <p class="mt-2 text-[#868e96]">
                Studied fundamental and advanced courses in Computer Science, including Data Structures & Algorithms, Object-Oriented Analysis & Design, and Database Systems.  
                Completed a final-year project focused on developing a real-world software application.
            </p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { onMounted } from "vue";
  import AOS from "aos";
  import "aos/dist/aos.css";
  
  onMounted(() => {
    AOS.refresh();
  });
  </script>
  
  <style scoped>
  /* Additional styling for responsiveness */
  @media (max-width: 768px) {
    .md\:grid-cols-2 {
      grid-template-columns: 1fr;
    }
  }
  </style>
  