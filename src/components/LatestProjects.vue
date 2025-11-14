<template>
  <section id="projects" class="text-white mt-20">
    <div class="text-center mb-12">
      <h2 class="text-4xl font-bold text-white">
        My
        <span
          class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-yellow-500"
        >
          Projects
        </span>
      </h2>
    </div>

    <ul
      class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
      data-aos="fade-right"
    >
      <li
        v-for="project in Projects"
        :key="project.id"
        class="rounded-xl overflow-hidden shadow-lg"
      >
        <!-- Imagen -->
        <div
          class="h-52 md:h-[24rem] rounded-t-xl relative group"
          :style="{
            backgroundImage: `url(${project.image})`,
            backgroundSize: 'cover',
            backgroundPosition: 'center'
          }"
        >
          <!-- Overlay -->
          <div
            class="overlay absolute inset-0 bg-[#181818] bg-opacity-0 hidden group-hover:flex group-hover:bg-opacity-80 items-center justify-center transition-all duration-500"
          >
            <!-- Link web -->
            <a
              v-if="project.webURL"
              :href="project.webURL"
              target="_blank"
              rel="noopener noreferrer"
              class="h-14 w-14 mr-2 border-2 border-[#ADB7BE] hover:border-white rounded-full flex items-center justify-center transition-all"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="h-8 w-8 text-[#ADB7BE] group-hover:text-white"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M17.25 6.75 22.5 12l-5.25 5.25M21 12H3"
                />
              </svg>
            </a>

            <!-- Link GitHub -->
            <a
              v-if="project.gitURL"
              :href="project.gitURL"
              target="_blank"
              rel="noopener noreferrer"
              class="h-14 w-14 border-2 border-[#ADB7BE] hover:border-white rounded-full flex items-center justify-center transition-all"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="h-8 w-8 text-[#ADB7BE] group-hover:text-white"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M2.036 12.322a1.012 1.012 0 010-.639C3.423 7.51 7.36 4.5 12 4.5s8.573 3.007 9.963 7.178a1.012 1.012 0 010 .639C20.577 16.49 16.64 19.5 12 19.5S3.427 16.49 2.036 12.322Z"
                />
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M15 12a3 3 0 11-6 0 3 3 0 016 0Z"
                />
              </svg>
            </a>
          </div>
        </div>

        <!-- Info -->
        <div class="bg-[#111a3e] p-4 border border-[#1f1641] rounded-b-xl">
          <h3 class="text-xl font-semibold text-white">{{ project.title }}</h3>
          <p class="text-gray-400 text-sm mt-2">{{ project.description }}</p>

          <div class="flex flex-wrap gap-2 mt-3">
            <span
              v-for="tech in project.technologies"
              :key="tech"
              class="px-2 py-1 text-xs rounded-md bg-[#1f2a48] text-gray-300"
            >
              {{ tech }}
            </span>
          </div>
        </div>
      </li>
    </ul>
  </section>
</template>


<script setup>
import { ref } from "vue";

const Projects = ref([
  {
    id: 1,
    category: "web development",
    image: "src/assets/notifications/notifications-service.png",
    title: "Notifications service",
    description: "Notifications service for mobile user and web users using FCM.",
    technologies: [".NET 8", "Firebase Cloud Messaging","MongoDB"]
  },
  {
    id: 2,
    category: "web development",
    image: "src/assets/estacion-2.png",
    title: "Weve business backend",
    description: "This service allows you to create electric charging stations and connect chargers to them.",
    technologies: [".NET 6","MongoDB", "Azure Blob Storage", "Azure DevOps"]
  },
  {
    id: 3,
    category: "web development",
    image: "src/assets/weve-admin.png",
    title: "Weve admin backend",
    description: "Platform that controls and monitors Weve business users.",
    technologies: [".NET 6","MongoDB"]
  },
  {
    id: 4,
    category: "web development",
    image: "src/assets/firmware-charger.png",
    title: "Firmware version management backend",
    description: "Backend to store, retrieve, delete, and manage electric charger firmware versions.",
    technologies: [".NET 8","Azure Blob Storage"]
  },
   {
    id: 5,
    category: "devops",
    image: "src/assets/grafana2.png",
    title: "Server monitoring service",
    description: "Server monitoring built with Grafana, Node Exporter, and Prometheus.",
    technologies: ["Docker","Grafana","Node exporter","Prometheus","Ubuntu"]
  }
]);
</script>
