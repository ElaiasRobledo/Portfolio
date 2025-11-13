<template>
  <div class="bg-[#0e0e14] min-h-screen relative">
    <NavBar />
    <HeroSection />
    <AboutSection />
    <ExperienceAndSkills />
    <LatesProjects />
    <Contact />
    <Footer />
    <Spinner :visible="isLoading" />
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { defineAsyncComponent } from 'vue';

const isLoading = ref(true);

const NavBar = defineAsyncComponent(() => import('@/components/NavBar.vue'));
const HeroSection = defineAsyncComponent(() => import('@/components/HeroSection.vue'));
const AboutSection = defineAsyncComponent(() => import('@/components/AboutSection.vue'));
const ExperienceAndSkills = defineAsyncComponent(() => import('@/components/ExperienceAndSkills.vue'));
const LatesProjects = defineAsyncComponent(() => import('@/components/LatestProjects.vue'));
const Contact = defineAsyncComponent(() => import('@/components/Contact.vue'));
const Footer = defineAsyncComponent(() => import('@/components/Footer.vue'));
const Spinner = defineAsyncComponent(() => import('@/components/Spinner.vue'));

onMounted(() => {
  // Simulación de carga
  setTimeout(() => {
    isLoading.value = false;
  }, 1500);
});
</script>
