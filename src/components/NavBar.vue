<template>
    <header class="font-mono flex justify-between items-center p-6 bg-opacity-50 relative z-20">
        <!-- Logo -->
        <div class="text-[#4D4D4D] text-3xl font-bold flex">MJ/MC</div>
        <!-- Mobile Toggle Button -->
        <div class="md:hidden z-30">
            <button type="button"
            class="block focus:outline-none"
            @click="isMenuOpen = !isMenuOpen">
                <span v-if="isMenuOpen" class="text-5xl">
                    <img src="https://img.icons8.com/ios-filled/100/4D4D4D/delete-sign.png" alt="close" width="50" height="50">
                </span>
                <span v-else class="text-5xl">
                    <img src="https://img.icons8.com/ios-filled/100/4D4D4D/menu--v6.png" alt="menu" width="50" height="50">
                </span>
            </button>
        </div>
        <!-- NavBar Link-->
         <nav
         :class="['fixed inset-0 z-20 flex flex-col items-center justify-center bg-[#fafafa] md:relative md:bg-transparent md:flex md:justify-between md:flex-row',
            isMenuOpen ? 'block':'hidden'
         ]">
            <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                <li v-for="item in Menu" :key="item.name">
                    <a href="item.href"
                    class="block text-[#4D4D4D] transition hover:text-[#4a5aec] ease-linear text-2xl md:text-lg"
                    @click.prevent="scrollToSection(item.href)">
                        {{ item.name }}
                    </a>
                </li>
            </ul>
            <!-- Dark Mode Toogle Button 
            <button
                @click="toggleDarkMode"
                class="hidden md:block p-2 rounded-lg bg-gray-200 dark:bg-gray-700 
                        text-gray-800 dark:text-gray-200 transition"
                >
                {{ isDark ? "☀️ Light" : "🌙 Dark" }}
            </button>-->
         </nav>
    </header>
</template>

<script setup>
import { ref, onMounted } from 'vue';
const Menu =ref([
    {name:'About', href:'#about'},
    {name:'Services', href:'#services'},
    {name:'Projects', href:'#projects'},
    {name:'Contact', href:'#contact'}
])

const isMenuOpen =ref(false)
const isDark = ref(false)

onMounted(() => {
    // Load theme from localStorage
    isDark.value = localStorage.getItem("theme") === "dark"
    document.documentElement.classList.toggle("dark", isDark.value)
})

const toggleDarkMode = () => {
    isDark.value = !isDark.value
    document.documentElement.classList.toggle("dark", isDark.value)
    localStorage.setItem("theme", isDark.value ? "dark" : "light")
}

const scrollToSection =(href)=>{
    isMenuOpen.value=false;
    const section=document.querySelector(href);
    if(section){
        section.scrollIntoView({behavior:'smooth'});
    }
}
</script>