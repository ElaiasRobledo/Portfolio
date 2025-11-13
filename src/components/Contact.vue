<template>
  <section class="text-white mt-20" id="contact">
    <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">
      Let's Connect
    </h2>

    <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
      <div>
        <p class="text-[#adb7be]">
          Si querés ponerte en contacto conmigo, te dejo mis redes y correo.
        </p>

        <div class="mt-8 space-y-8">

          <!-- LinkedIn -->
          <div class="flex items-center">
            <div
              class="p-2 flex justify-center items-center rounded-full border border-[#111a3e]"
              style="background:#111a3e;width:50px;height:46px;backdrop-filter:blur(9px);-webkit-backdrop-filter:blur(9px);"
            >
              <img
                src="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png"
                alt="LinkedIn"
                class="w-6 h-6"
              />
            </div>
            <div class="ml-5">
              <h4 class="font-semibold">LinkedIn</h4>
              <a
                href="https://www.linkedin.com/in/elias-robledo"
                target="_blank"
                class="text-[#adb7be] hover:text-primary transition"
              >
                linkedin.com/in/elias-robledo
              </a>
            </div>
          </div>

          <!-- GitHub -->
          <div class="flex items-center">
            <div
              class="p-2 flex justify-center items-center rounded-full border border-[#111a3e]"
              style="background:#111a3e;width:50px;height:46px;backdrop-filter:blur(9px);-webkit-backdrop-filter:blur(9px);"
            >
              <img
                src="https://img.icons8.com/ios-filled/50/ffffff/github.png"
                alt="GitHub"
                class="w-6 h-6"
              />
            </div>
            <div class="ml-5">
              <h4 class="font-semibold">GitHub</h4>
              <a
                href="https://github.com/eliasrobledo"
                target="_blank"
                class="text-[#adb7be] hover:text-primary transition"
              >
                github.com/eliasrobledo
              </a>
            </div>
          </div>

          <!-- Email -->
          <div class="flex items-center">
            <div
              class="p-2 flex justify-center items-center rounded-full border border-[#111a3e]"
              style="background:#111a3e;width:50px;height:46px;backdrop-filter:blur(9px);-webkit-backdrop-filter:blur(9px);"
            >
              <img
                src="https://img.icons8.com/ios-filled/50/ffffff/new-post.png"
                alt="Email"
                class="w-6 h-6"
              />
            </div>
            <div class="ml-5">
              <h4 class="font-semibold">Email</h4>
              <a
                href="mailto:elias.robledo@example.com"
                class="text-[#adb7be] hover:text-primary transition"
              >
                elias.robledo@example.com
              </a>
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
