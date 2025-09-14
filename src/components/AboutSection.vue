<template>
    <section class="font-mono text-[#4d4d4d] mt-18" id="about">
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="font-mono text-4xl font-bold text-[#4d4d4d] mb-8 text-left">Tech Stack</h2>
                <p class="font-mono text-[#4d4d4d] font-semibold">These are the tools that I use for my development.</p>
                <div class="space-y-8 py-8">
                    <div v-for="techs in techstack" :key="techs.id"
                    class="flex items-center md:w-[80%] w-full rounded-xl bg-[#fafafa] shadow-lg border border-[#4d4d4d]">
                        <div class="ml-7 w-1/4">
                            <img :src="techs.icon" :alt="techs.name">
                        </div>
                        <div class="w-3/2 pl-4">
                            <h3 class="font-mono text-2xl font-semibold lg:text-xl bg-clip-text">
                                {{ techs.name }}
                            </h3>
                            <p class="font-mono text-[#4d4d4d] mr-3">
                                {{ techs.description }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="font-mono text-4xl font-bold text-[#4d4d4d] md:text-center mb-4 text-left">About Me</h2>
                <p class="font-mono text-base lg:text-lg mt-8 py-8">
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui facere libero cupiditate fugit minima voluptates numquam est eos voluptate saepe eius amet harum provident accusamus omnis sit in cum incidunt dolorum, necessitatibus illo reiciendis ipsam debitis velit! Itaque officia architecto fugit, cum dolorum eos dolore quaerat quis nobis id similique!<br/>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui facere libero cupiditate fugit minima voluptates numquam est eos voluptate saepe eius amet harum provident accusamus omnis sit in cum incidunt dolorum, necessitatibus illo reiciendis ipsam debitis velit! Itaque officia architecto fugit, cum dolorum eos dolore quaerat quis nobis id similique!<br/>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui facere libero cupiditate fugit minima voluptates numquam est eos voluptate saepe eius amet harum provident accusamus omnis sit in cum incidunt dolorum, necessitatibus illo reiciendis ipsam debitis velit! Itaque officia architecto fugit, cum dolorum eos dolore quaerat quis nobis id similique!
                </p>
                <div class="lg:ml-[25%] grid grid-cols-2 gap-4 max-w-lg pt-8">
                    <div class="text-center rounded-xl bg-[#fafafa] shadow-lg border border-[#4d4d4d] p-3">
                        <h3 class="font-mono text-[#4d4d4d] font-bold text-xl sm:text-2xl lg:text-3xl">+15</h3>
                        <p class="font-mono text-sm sm:text-base text-[#4d4d4d]">Happy Client</p>
                    </div>
                    <div class="text-center rounded-xl bg-[#fafafa] shadow-lg border border-[#4d4d4d] p-3">
                        <h3 class="font-mono text-[#4d4d4d] font-bold text-xl sm:text-2xl lg:text-3xl">+21</h3>
                        <p class="font-mono text-sm sm:text-base text-[#4d4d4d]">Projects</p>
                    </div>
                    <div class="text-center rounded-xl bg-[#fafafa] shadow-lg border border-[#4d4d4d] p-3">
                        <h3 class="font-mono text-[#4d4d4d] font-bold text-xl sm:text-2xl lg:text-3xl">+6</h3>
                        <p class="font-mono text-sm sm:text-base text-[#4d4d4d]">Years Experience</p>
                    </div>
                    <div class="text-center rounded-xl bg-[#fafafa] shadow-lg border border-[#4d4d4d] p-3">
                        <h3 class="font-mono text-[#4d4d4d] font-bold text-xl sm:text-2xl lg:text-3xl">+200</h3>
                        <p class="font-mono text-sm sm:text-base text-[#4d4d4d]">Cups of Coffee</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import {ref} from 'vue';
const techstack=ref([
    {
        id: 1,
        icon: 'https://img.icons8.com/external-tal-revivo-color-tal-revivo/60/external-vuejs-an-open-source-javascript-framework-for-building-user-interfaces-and-single-page-applications-logo-color-tal-revivo.png',
        name: 'VueJS',
        description: 'An open-source, progressive JavaScript framework for building user interfaces and single-page applications. It is known for its approachability, performance, and versatility.'
    },
    {
        id: 2,
        icon: 'https://img.icons8.com/fluency/60/vite.png',
        name: 'Vite',
        description: 'A lightning-fast frontend build tool that provides instant server startup, hot module replacement, and optimized builds for modern web applications.'
    },
    {
        id: 3,
        icon: 'https://img.icons8.com/external-tal-revivo-shadow-tal-revivo/60/external-django-a-high-level-python-web-framework-that-encourages-rapid-development-logo-shadow-tal-revivo.png',
        name: 'Django',
        description: 'It provides a structured environment and pre-built components for common web development tasks, such as database interaction, user authentication, and content administration.'
    },
    {
        id: 4,
        icon: 'https://img.icons8.com/fluency/60/tailwind_css.png',
        name: 'Tailwind CSS',
        description: 'A utility-first CSS framework for rapidly building custom user interfaces. Tailwind CSS offers a comprehensive set of low-level utility classes that directly apply individual CSS properties.'
    },
    {
        id: 5,
        icon: 'https://img.icons8.com/material/60/vercel.png',
        name: 'Vercel',
        description: 'A cloud platform, often described as a "frontend cloud," that empowers developers to build, deploy, and scale fast, secure, and personalized web experiences with a focus on frontend frameworks.'
    },
])
</script>