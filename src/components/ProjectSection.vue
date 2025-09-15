<template>
    <section class="font-mono text-[#4d4d4d] mt-20" id="projects">
        <div class="px-4 xl:pl-16">
            <div class="mb-4 flex justify-center xl:pr-16">
                <div class="flex space-x-4 mb-4 mt-5 md:mt-0">
                    <button class="cursor-pointer text-2xl hover:text-[#4a5aec]" v-for="category in ['All', 'Web App', 'Mobile App']"
                    :key="category" @click="() => selectedCategory = category">
                        {{ category }}
                    </button>
                </div>
            </div>
            <ul class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols2 md:gap-10 md:pt-12 lg:grid-cols-3" data-aos="fade-right">
                <div v-for="project in filteredProjects" :key="project.id">
                    <div class="h-52 md:h-[24rem] rounded-t-xl relative group" :style="{backgroundImage: 'url('+project.image+')', backgroundSize:'cover'}">
                        <div class="overlay items-center justify-center absolute top-0 left-0 w-full h-full bg-[#18181880] bg-opacity-0
                        hidden group-hover:flex group-hover:bg-opacity-0 transition-all duration-500">
                            <a :href="project.webURL" class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#818181] hover:border-white group/link">
                                <svg xmlns="http://www.w3.org/2000svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true" data-slot="icon" class="h-10 w-10 text-[#adb7be] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-point">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 6.75 22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3-4.5 16.5">
                                    </path>
                                </svg>
                            </a>
                            <a :href="project.gitURL" class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#818181] hover:border-white group/link">
                                <svg xmlns="http://www.w3.org/2000svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true" data-slot="icon" class="h-10 w-10 text-[#adb7be] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-point">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.036 12.322a1.012 1.012 0 0 1 0-.644C3.421 7.51 7.356 4.5 12 4.5c4.64 0 8.574 3.01 9.963 7.178.07.207.07.437 0 .644C20.574 16.49 16.64 19.5 12 19.5c-4.644 0-8.579-3.01-9.964-7.178Z">
                                    </path>
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z">
                                    </path>
                                </svg>
                            </a>
                        </div>
                    </div>
                    <div class="text-[#4d4d4d] rounded-b-xl mt-3 bg-[#fafafa] shadow-lg border border-[#4d4d4d] py-6 px-4">
                        <h3 class="text-lg font-semibold uppercase lg:text-xl">{{ project.title }}</h3>
                        <p class="text-[#4d4d4d]">{{ project.description }}</p>
                        <div class="flex flex-wrap p-2.5">
                            <div v-for="technology in project.technologies" :key="technology"
                            class="text-center ml-1 mt-1 rounded-3xl bg-[#fafafa]"
                            style="box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1); border: 1px solid #111827;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                                <p class="px-1 py-2">{{ technology }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </ul>
        </div>
    </section>
</template>

<script setup>
import {ref,computed} from 'vue';
const Projects =ref([
    {
        id:1,
        category:'Web App',
        image: 'https://i.pinimg.com/736x/a1/37/89/a13789d47818c18e3aaa332d0cd327a0.jpg',
        title: 'Project 1',
        description: 'my Description',
        technologies: ['VueJS', 'Vite', 'Tailwind CSS'],
        gitURL: '',
        webURL: ''
    },
    {
        id:2,
        category:'Web App',
        image: 'https://i.pinimg.com/736x/a1/37/89/a13789d47818c18e3aaa332d0cd327a0.jpg',
        title: 'Project 2',
        description: 'my Description',
        technologies: ['Django'],
        gitURL: '',
        webURL: ''
    },
    {
        id:3,
        category:'Mobile App',
        image: 'https://img.freepik.com/premium-photo/program-designer-developer-ai-generative_199064-2134.jpg',
        title: 'Project 3',
        description: 'my Description',
        technologies: ['VueJS'],
        gitURL: '',
        webURL: ''
    },
    {
        id:4,
        category:'Web App',
        image: 'https://i.pinimg.com/736x/a1/37/89/a13789d47818c18e3aaa332d0cd327a0.jpg',
        title: 'Project 4',
        description: 'my Description',
        technologies: ['HTML', 'CSS'],
        gitURL: '',
        webURL: ''
    }
]);
const selectedCategory =ref('All');
const filteredProjects =computed(()=>{
    if(selectedCategory.value === 'All'){
        return Projects.value;
    }else{
        return Projects.value.filter(project => project.category.toLocaleLowerCase() === selectedCategory.value.toLocaleLowerCase());
    }
})
</script>