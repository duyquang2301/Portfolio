<template>
    <section id="projects" class="mt-20 bg-gray-100" data-aos="fade-up">

        <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-[#868e96] text-left mb-8" data-aos="fade-up"
                :style="{ fontFamily: 'Grechen Fuemen, sans-serif' }">
                Projects
            </h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3">
            <div v-for="project in projects" :key="project.id" class="bg-white rounded-lg shadow-lg overflow-hidden">
                <img :src="project.image" :alt="project.title" class="w-full h-48 object-cover">
                <div class="p-6">
                    <h3 class="text-xl font-semibold">{{ project.title }}</h3>
                    <p class="text-gray-600 mt-2">{{ project.description }}</p>
                    <a v-if="project.display" :href="project.link" target="_blank"
                        class="block mt-4 text-blue-500 hover:underline">
                        View Project →
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const projects = ref([
    {
        id: 1,
        title: "HIRE IT",
        description: "Hire-IT is a job recruitment platform designed for both job seekers and employers.",
        image: "https://duws858oznvmq.cloudfront.net/Direct_hire_and_permanent_hire_6945df5904.webp", // Replace with actual image
        link: "https://github.com/duyquang2301/hire-it-fe",
        display: true
    },
    {
        id: 2,
        title: "E-commerce API",
        description: "This API provides backend functionalities for an e-commerce platform, including user authentication, product management, order processing, and payment integration.",
        image: "https://cdn2.fptshop.com.vn/unsafe/1920x0/filters:quality(100)/2023_12_27_638393109771583706_e-commerce-la-gi-3.jpg",
        link: "https://github.com/duyquang2301/E_Commerce_Backend",
        display: true
    },
    {
        id: 3,
        title: "Project External",
        description: "Built a real-time chat app with media support, AWS S3, webhooks, and optimized backend using Lambda, SQS, and Jest.",
        image: "https://developers.line.biz/assets/img/messaging-api-architecture.f40bffbb.png",
        link: "https://your-project-link.com",
        display: false
    }
]);
</script>

<style scoped>
/* Add custom styles here if needed */
</style>