<template>
<section id="about" class="text-white mt-18">
  <div class="flex flex-col items-center justify-center py-16 px-4 xl:px-16 text-center">

    <h2 class="text-4xl font-bold mb-6">
      More <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">About</span> Me
    </h2>

    <p class="max-w-3xl text-base lg:text-lg text-gray-300">
      Qui facere libero cupiditate fugit minima voluptates numquam est eos voluptate saepe
      eius amet harum provident accusamus omnis sit cum incidunt dolorum, necessitatibus
      illo reiciendis ipsam debitis velit! Itaque officia architecto fugit, cum dolorum eos
      dolore quaerat quis nobis id similique!
    </p>

    <div class="grid grid-cols-1 sm:grid-cols-3 gap-6 max-w-3xl pt-12 w-full">
      <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
        <h3 class="counter text-white font-bold text-3xl" data-target="200">0</h3>
        <p class="text-sm text-gray-300">Happy Client</p>
      </div>

      <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
        <h3 class="counter text-white font-bold text-3xl" data-target="300">0</h3>
        <p class="text-sm text-gray-300">Project</p>
      </div>

      <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-4">
        <h3 class="counter text-white font-bold text-3xl" data-target="200">0</h3>
        <p class="text-sm text-gray-300">Happy Client</p>
      </div>
    </div>
  </div>
</section>


</template>

<script setup>
import { ref } from 'vue';
import { onMounted } from 'vue';

onMounted(() => {
  const counters = document.querySelectorAll('.counter')
  const speed = 60 // velocidad (cuanto menor, más rápido)

  const animate = (counter) => {
    const target = +counter.getAttribute('data-target')
    const value = +counter.innerText
    const increment = Math.ceil(target / speed)

    if (value < target) {
      counter.innerText = value + increment
      requestAnimationFrame(() => animate(counter))
    } else {
      counter.innerText = target
    }
  }

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
        University: 'Universidad Tecnologica Nacional',
        program: 'Software Development'
    }
]);

</script>