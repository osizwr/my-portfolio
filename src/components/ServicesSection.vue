<template>
    <section class="text-[#4d4d4d] mt-20" id="services">
        <div class="px-4 xl:pl-16">
            <h2 class="font-mono text-4xl font-bold text-[#4d4d4d] mb-4 text-center">My Services</h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-4">
            <div v-for="service in services" :key="service.id" data-aos="fade-up"
            class="px-8 py-12 rounded-xl bg-[#fafafa] shadow-lg border border-[#4d4d4d]">
                <div class="mx-auto h-24 text-center xl:h-28 xl:w-28">
                    <div>
                        <img :src="service.icon" :alt="service.name">
                    </div>
                </div>
                <div class="text-center">
                    <h3 class="font-mono pt-8 text-lg font-semibold uppercase bg-clip-text text-[#4d4d4d] lg:text-xl">
                        {{ service.name }}
                    </h3>
                    <p class="text-mono text-[#4d4d4d] pt-4 text-sm md:text-base">
                        {{ service.description }}
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
        icon: 'https://img.icons8.com/ios-filled/100/4d4d4d/google-code.png',
        name: 'Web Development',
        description: 'this is my description'
    },
    {
        id:2,
        icon: 'https://img.icons8.com/ios-filled/100/4d4d4d/web-design.png',
        name: 'Web Design',
        description: 'this is my description'
    },
    {
        id:3,
        icon: 'https://img.icons8.com/ios-filled/100/4d4d4d/two-smartphones.png',
        name: 'Mobile Development',
        description: 'this is my description'
    },
    {
        id:4,
        icon: 'https://img.icons8.com/ios-filled/100/4d4d4d/windows10-personalization.png',
        name: 'Graphic Design',
        description: 'this is my description'
    },
])
</script>