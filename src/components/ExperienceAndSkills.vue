<template>

    <section id="experience" class="text-white mt-18"> <!-- Fondo decorativo -->
        <div class="absolute right-0 top-0 h-full w-full justify-end">
            <span class="flex opacity-20">
                <span class="w-16 h-32 rounded-l-full flex bg-primary blur-2xl"></span>
                <span class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"></span>
            </span>
        </div>

        <!-- Skills -->
        <div data-aos="flip-left" class="mt-16 flex flex-col items-center">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
                <h1 class="text-4xl font-bold text-white mb-4 text-left md:text-center">
                    My
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-green-300 to-secondary">Skills</span>
                </h1>

                <div class="mt-8" v-for="skill in Skills" :key="skill.id">
                    <div class="flex items-end justify-between">
                        <h4 class="font-semibold uppercase text-white">{{ skill.name }}</h4>
                        <h3 class="text-2xl font-bold text-white">{{ skill.width }}</h3>
                    </div>
                    <div class="mt-2 h-1 w-full bg-[#131d30] rounded-full">
                        <div class="h-1 rounded-full bg-primary skill-bar" :data-width="skill.width" style="width: 0">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Experiences -->
        <div data-aos="flip-left" class="mt-16 flex flex-col items-center">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%] mx-auto">
                <h1 class="text-4xl font-bold text-white mb-4 text-left md:text-center">
                    My
                    <span
                        class="text-transparent bg-clip-text bg-gradient-to-r from-white to-green-500">Experiences</span>
                </h1>
            </div>

            <div class="space-y-8 py-8 w-[80%] mx-auto">
                <div v-for="element in Experiences" :key="element.id"
                    class="flex items-center rounded-xl p-4 bg-[#111a3e] shadow-lg border border-[#1f1641]">
                    <div class="w-1/4 flex justify-center">
                        <img src="https://vulletic.com.ar/wp-content/uploads/2024/06/Vulletic_logo.png" alt="icon" />
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3
                            class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ element.role }}
                        </h3>
                        <p class="text-white">{{ element.company }}</p>
                        <p class="text-gray-300">{{ element.date }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>


<script setup>

//AGREGAR EXPERIENCIAS Y TEECH STACK
import { ref } from 'vue';
import { onMounted } from "vue";

onMounted(() => {
    const bars = document.querySelectorAll(".skill-bar")

    const observer = new IntersectionObserver(
        entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const el = entry.target
                    el.style.width = el.getAttribute("data-width")
                    el.style.transition = "width 1.5s ease-in-out"
                    observer.unobserve(el)
                }
            })
        },
        { threshold: 0.3 }
    )

    bars.forEach(bar => observer.observe(bar))
})
const Skills = ref([
    
    {
        id: 1,
        name: 'Proactivity',
        width: '100%'

    },
    {
        id: 2,
        name: 'Team Work',
        width: '100%'

    },
     {
        id: 3,
        name: 'Creativity',
        width: '100%'

    },
    {
        id: 4,
        name: '.NET',
        width: '86%'

    },
    {
        id: 5,
        name: 'Aspire',
        width: '27%'
    },
        {
        id: 6,
        name: 'Blazor',
        width: '44%'
    },
    {
        id: 7,
        name: 'Linux system administration (Debian-based)',
        width: '69%'
    },
    {
        id: 8,
        name: 'MongoDB',
        width: '81%'
    },
    {
        id: 6,
        name: 'PostgreSQL',
        width: '51%'
    }
])
const Experiences = ref([
    {
        id: 1,
        role: 'Backend developer',
        company: 'Vulletic EV Chargers',
        date: 'October 2022 - At present'
    }
])

</script>