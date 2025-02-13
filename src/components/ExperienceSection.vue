<template >
    <section class="text-white mt-20" id="experience">
        <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-[#868e96] text-left mb-8" data-aos="fade-up"
              :style="{ fontFamily: 'Grechen Fuemen, sans-serif' }">
            My Experience
          </h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3">
            <div v-for="service in services" :key="service.id" data-aos="fade-up"
            class="px-8 py-12 rounded-xl bg-[#ffffff] shadow-lg border border-[#0e0431]"
            >
                <div class="mx-auto h-24 w-24 text-center xl:h-20 xl:w-20">
                    <div>
                        <img :src="service.icon" alt="service icon">
                    </div>
                </div>
                <div class="text-center">
                    <h3 class="pt-4 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                        {{ service.company }}
                    </h3>
                    <p class="text-[#868e96] pt-4 text-sm group-hover:text-white md:text-base">
                        {{ service.role }}
                    </p>
                    <p class="text-[#868e96] pt-4 text-sm group-hover:text-white md:text-base">
                        {{ service.duration }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import {ref} from 'vue';
const services =ref([
    {
        id:1,
        icon:'https://www.supremetech.vn/wp-content/uploads/2023/03/logo_CM.png',
        role: "Software Engineer",
        company: "ClassMethod Da Nang",
        duration: "Nov 2023 - Present",
    },
    {
        id:2,
        icon:'https://www.supremetech.vn/wp-content/themes/stwp/images/ST-Logo-Blue.svg',
        role: "Intern",
        company: "SupremeTech",
        duration: "Aug 2023 - Nov 2023",
    },
    ])
</script>
