<template>
    <section class="text-white mt-20" id="services" >
      <div class="px-4 xl:pl-16">
        <h2 class="text-4xl font-bold text-[#868e96] mb-4 italic" :style="{ fontFamily: 'Grechen Fuemen, sans-serif' }">Skills</h2>
      </div>
      
      <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 sm:grid-cols-2 gap-6 pt-10 md:gap-10">
        <!-- Left Column: Image -->
        <div data-aos="fade-up" class="img-container flex justify-center">
          <img src="@/assets/developerActivity.svg" alt="Service" class="w-full max-w-md rounded-lg" />
        </div>
  
        <!-- Right Column: Text -->
        <div v-if="skillsSection.display" data-aos="fade-up" class="text-container px-8 py-12 rounded-xl">
          <h3 class="text-2xl font-semibold text-black">{{ skillsSection.title }}</h3>
        
          <p class="mt-4 text-[#868e96]">
           {{ skillsSection.subTitle }}
          </p>
         
          <ul class="list-disc pl-5 text-[#868e96]">
            <font-awesome-icon icon="fa-solid fa-house" />
            <p v-for="(skill, index) in skillsSection.skills" :key="index">
              {{ skill }}
            </p>
          </ul>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { onMounted, ref } from "vue";
  import AOS from "aos";
  import "aos/dist/aos.css";
  
  onMounted(() => {
    AOS.refresh();
  });

  const skillsSection = ref({
  title: "What I do",
  subTitle: "PASSIONATE BACKEND DEVELOPER WHO LOVES TO BUILD SCALABLE AND SECURE SYSTEMS",
  skills: [
    "⚡ Design and implement APIs and microservices for web and mobile applications",
    "⚡ Build scalable server-side architectures using Node.js, Java Spring and other modern back-end technologies",
    "⚡ Integration of cloud services like AWS, Firebase for seamless deployments and scalability"
  ],
  softwareSkills: [
    { skillName: "html-5", fontAwesomeClassname: "fab fa-html5" },
    { skillName: "css3", fontAwesomeClassname: "fab fa-css3-alt" },
    { skillName: "sass", fontAwesomeClassname: "fab fa-sass" },
    { skillName: "JavaScript", fontAwesomeClassname: "fab fa-js" },
    { skillName: "reactjs", fontAwesomeClassname: "fab fa-react" },
    { skillName: "nodejs", fontAwesomeClassname: "fab fa-node" },
    { skillName: "swift", fontAwesomeClassname: "fab fa-swift" },
    { skillName: "npm", fontAwesomeClassname: "fab fa-npm" },
    { skillName: "sql-database", fontAwesomeClassname: "fas fa-database" },
    { skillName: "aws", fontAwesomeClassname: "fab fa-aws" },
    { skillName: "firebase", fontAwesomeClassname: "fas fa-fire" },
    { skillName: "python", fontAwesomeClassname: "fab fa-python" },
    { skillName: "docker", fontAwesomeClassname: "fab fa-docker" }
  ],
  display: true
});
  </script>
  
  