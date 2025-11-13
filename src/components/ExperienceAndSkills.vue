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
                <h1 class="text-5xl font-bold text-white text-left mb-4">
                    My
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">Skills</span>
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
                <h1 class="text-5xl font-bold text-white mb-4 text-left md:text-center">
                    My
                    <span
                        class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">Experiences</span>
                </h1>
            </div>

            <div class="space-y-8 py-8 w-[80%] mx-auto">
                <div v-for="element in Experiences" :key="element.id"
                    class="flex items-center rounded-xl p-4 bg-[#111a3e] shadow-lg border border-[#1f1641]">
                    <div class="w-1/4 flex justify-center">
                        <img src="https://img.icons8.com/ios-filled/100/ffffff/lawyer.png" alt="icon" />
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
        name: '.NET',
        width: '80%'

    },
    {
        id: 2,
        name: 'Linux',
        width: '50%'
    }
])
const Experiences = ref([
    {
        id: 1,
        role: 'Backend developer',
        company: 'Vulletic EV Chargers',
        date: 'October 2022'
    }
])

</script>