<template>
  <section id="about" class="text-white mt-18">
    <div class="flex flex-col items-center justify-center py-16 px-4 xl:px-16 text-center">

      <div class="text-center" data-aos="flip-right">
        <div class="space-y-8 py-8 text-white text-left mb-8">
          <h2 class="text-4xl font-bold text-center">My <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-secondary"> Education</span></h2>

          <div v-for="element in education" :key="element.id"
            class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
            <div class="w-1/4 flex justify-center">
              <img src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation cap">
            </div>

            <div class="w-3/4 pl-4">
              <h3
                class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                {{ element.school }}
              </h3>
              <p class="text-white">{{ element.program }}</p>
              <p class="text-white">{{ element.year }}</p>
            </div>
          </div>
        </div>
      </div>

      <h2 class="text-4xl font-bold mb-6">
        More <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">About</span> Me
      </h2>

      <p class="max-w-3xl text-base lg:text-lg text-gray-300">
      I’m a young developer born in Argentina who loves music and computing.
      I’m a person curious and passionate  about technologies. 
      I seek to grow as a professional and  as a person, contributing  in different projects and learning from talented and experienced people.
      </p>

      <div class="grid grid-cols-1 sm:grid-cols-3 gap-6 max-w-3xl pt-12 w-full">
        <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
          <h3 class="counter text-white font-bold text-3xl">∞</h3>
          <p class="text-sm text-gray-300">Happy Clients</p>
        </div>

        <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
          <h3 class="counter text-white font-bold text-3xl"> +5</h3>
          <p class="text-sm text-gray-300">Projects</p>
        </div>

        <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
          <h3 class="counter text-white font-bold text-3xl">3</h3>
          <p class="text-sm text-gray-300">Years of experience</p>
        </div>
      </div>
    </div>
  </section>


</template>

<script setup>
import { ref } from 'vue';
import { onMounted } from 'vue';

onMounted(() => {

  const observer = new IntersectionObserver((entries, obs) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        counters.forEach(counter => animate(counter))
        obs.disconnect() // se ejecuta solo una vez
      }
    })
  }, { threshold: 0.5 })

  observer.observe(document.querySelector('#about')) // id de tu sección
});
const education = ref([
  {
    id: 1,
    school: 'national technological university (UTN FRSFCO)',
    program: 'Software Development',
    year:'March 2021 - May 2024'
  }
]);

</script>