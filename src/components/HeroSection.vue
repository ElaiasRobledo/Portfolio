<template>
  <section class="relative w-full">
    <!-- Fondo decorativo (z-[-1] para no bloquear clics) -->
    <div class="absolute top-0 inset-x-0 h-64 flex items-start z-[-1]">
      <div class="h-24 w-2/3 bg-gradient-to-br from-[#570cac] blur-2xl opacity-40">
        <div class="h-20 w-3/5 bg-gradient-to-r from-[#670ccf] opacity-40 blur-2xl"></div>
      </div>
    </div>

    <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg lg:max-w-screen-xl mx-auto relative z-10">
      <div class="grid lg:grid-cols-2 gap-10 cl:gap-14 relative pt-24 lg:max-w-3xl mx-auto">
        <!-- Texto principal -->
        <div class="lg:py-6">
          <div class="text-center lg:text-left">
            <h1 class="pt-4 text-white font-bold text-4xl md:text-5xl lg:text-6xl">
              Hi! I'm
              <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-green-100">
                Elias Robledo
              </span>
            </h1>
          </div>

          <p class="text-gray-300 pt-8 text-center lg:text-left mx-auto max-w-xl">
            Descripcion sobre mi
          </p>

          <!-- Botones -->
          <div class="flex items-center gap-3 pt-9 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
            <!-- Hire Me -->
            <button
              @click="scrollToContact"
              class="px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center overflow-hidden cursor-pointer"
            >
              <span
                class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-primary border-2 border-transparent"
              ></span>
              <span class="relative flex items-center justify-center text-white font-semibold">Hire Me</span>
            </button>

            <!-- Download Resume -->
            <a
              href="/CV-EliasRobledo.pdf"
              download
              class="border border-primary px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center transition-all hover:scale-105 text-primary font-semibold cursor-pointer"
            >
              <svg
                width="18"
                height="22"
                viewBox="0 0 18 22"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="mr-2"
              >
                <path
                  d="M13 9L9 13M9 13L5 9M9 13V1"
                  stroke="#f59e0b"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M1 17V18C1 19.6569 2.34315 21 4 21H14C15.6569 21 17 19.6569 17 18V17"
                  stroke="#f59e0b"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
              Download Resume
            </a>
          </div>
        </div>

        <!-- Imagen -->
        <div class="flex w-full h-96 lg:h-full items-center relative z-10">
          <div
            class="absolute z-0 top-1/2 -translate-y-1/2 w-full h-[calc(80%+20px)] bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl"
          ></div>

          <div class="relative z-10 mx-auto p-2 rounded-full shadow-lg border border-primary">
            <img
              src="@/assets/eliaspic.jpg"
              alt="Hero pic"
              class="w-64 h-64 lg:w-80 lg:h-80 rounded-full object-cover"
              loading="lazy"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const scrollToContact = () => {
  const contactSection = document.querySelector('#contact');
  if (contactSection) {
    contactSection.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>
