<template>
  <footer class="bg-[#0d1224] border-t border-[#1f1641] py-8 text-gray-300 mt-16">
    <div class="max-w-screen-xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-4">
      <p class="text-sm text-center md:text-left">
        © {{ new Date().getFullYear() }} 
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary font-semibold">
          Elias Robledo
        </span>. 
        All rights reserved.
      </p>

      <div class="flex items-center gap-4">
        <a href="https://github.com/" target="_blank" class="hover:text-primary transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" class="h-5 w-5">
            <path
              d="M12 .5C5.648.5.5 5.648.5 12c0 5.086 3.292 9.39 7.86 10.914.575.107.784-.25.784-.557 0-.273-.01-.997-.015-1.957-3.197.695-3.872-1.54-3.872-1.54-.523-1.33-1.278-1.685-1.278-1.685-1.045-.714.08-.699.08-.699 1.155.082 1.763 1.186 1.763 1.186 1.028 1.762 2.697 1.253 3.355.959.103-.745.403-1.253.732-1.54-2.552-.29-5.236-1.276-5.236-5.677 0-1.255.45-2.28 1.186-3.083-.118-.29-.514-1.46.113-3.043 0 0 .964-.308 3.161 1.176a10.905 10.905 0 012.878-.388c.976.004 1.958.132 2.878.388 2.197-1.484 3.16-1.176 3.16-1.176.629 1.583.233 2.753.115 3.043.738.803 1.186 1.828 1.186 3.083 0 4.412-2.688 5.383-5.252 5.668.414.362.783 1.086.783 2.193 0 1.582-.014 2.856-.014 3.242 0 .311.206.672.79.556C20.713 21.387 24 17.086 24 12 24 5.648 18.852.5 12 .5z"
            />
          </svg>
        </a>

        <a href="https://linkedin.com/" target="_blank" class="hover:text-primary transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" class="h-5 w-5">
            <path
              d="M20.447 20.452h-3.554V14.8c0-1.345-.026-3.078-1.878-3.078-1.88 0-2.169 1.462-2.169 2.973v5.757H9.292V9.003h3.414v1.561h.049c.477-.9 1.637-1.848 3.371-1.848 3.605 0 4.271 2.373 4.271 5.457v6.279zM5.337 7.433a2.062 2.062 0 01-2.062-2.06A2.061 2.061 0 015.337 3.31a2.06 2.06 0 012.06 2.063 2.061 2.061 0 01-2.06 2.06zM6.934 20.452H3.74V9.003h3.194v11.449zM22.225 0H1.771C.792 0 0 .774 0 1.727v20.545C0 23.227.792 24 1.771 24h20.451C23.207 24 24 23.227 24 22.272V1.727C24 .774 23.207 0 22.225 0z"
            />
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>
