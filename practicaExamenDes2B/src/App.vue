<script setup>
import { ref } from 'vue';

let contH = ref(20)
let contD = ref(3)

function sumarCorazon() {
  if (contH.value == 20) {
    contH.value++
    contD.value = 3
  }
}

function sumarDislike() {
  if (contD.value == 3) {
    contD.value++
    contH.value = 20
  }
}

</script>

<template>
  <div class="mx-[20%]">
    <div class="my-8 shadow shadow-gray-500 bg-slate-100 h-[1000px] px-[5%] py-[6%]">
      <div class="flex justify-between mb-4">
        <p class="font-bold text-lg text-gray-700">Historias</p>
        <p class="text-white bg-blue-400 rounded px-1 py-0">Todas</p>
      </div>

      <div class="flex justify-between mb-4">
        <div class="h-[22%] w-[22%]">
          <img class=" rounded-3xl border-4 border-blue-700" src="https://i.redd.it/t1qvlui8nw7b1.jpg" alt="">
          <p class="text-gray-400 ml-4 mt-1 font-semibold">CADE</p>
        </div>
        <div class="h-[22%] w-[22%]">
          <img class=" rounded-3xl border-4 border-blue-700" src="https://i.pinimg.com/564x/9b/bb/de/9bbbde4c554c7f1c6528d28e64b934f2.jpg" alt="">
          <p class="text-gray-400 ml-4 mt-1 font-semibold">CADE</p>
        </div>
        <div class="h-[22%] w-[22%]">
          <img class=" rounded-3xl border-4 border-gray-500" src="https://i.redd.it/t1qvlui8nw7b1.jpg" alt="">
          <p class="text-gray-400 ml-4 mt-1 font-semibold">CADE</p>
        </div>
        <div class="h-[22%] w-[22%]">
          <img class=" rounded-3xl border-4 border-gray-500" src="https://i.pinimg.com/564x/9b/bb/de/9bbbde4c554c7f1c6528d28e64b934f2.jpg" alt="">
          <p class="text-gray-400 ml-4 mt-1 font-semibold">CADE</p>
        </div>
      </div>

      <div class="flex justify-between mb-4">
        <div class="flex h-[8%]">
          <img class="h-[8%] w-[8%] rounded-full" src="https://i.kym-cdn.com/photos/images/original/001/712/873/dd0.jpg" alt="">
          <div class="ml-4">
            <p class="font-bold text-gray-700 text-lg">Santiago Antonio</p>
            <p class="font-bold text-gray-400 text-sm">Hace 10 minutos</p>
          </div>
        </div>
        <div class="mt-[4%]">
          <p class="font-bold text-red-500">Reportar</p>
        </div>
      </div>

      <div class="flex justify-center">
        <img class="h-[100%] w-[100%] rounded-3xl" src="https://www.hillspet.es/content/dam/cp-sites/hills/hills-pet/en_us/exported/dog-care/new-pet-parent/images/golden-retriever-puppy-running-outside.jpg" alt="">
      </div>

      <div class="flex mt-2 mb-4">
        <div class="flex">
          <svg @click="sumarCorazon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
          </svg>
          <p class="ml-1">{{ contH }}</p>
        </div>
        <div class="flex ml-6">
          <svg @click="sumarDislike" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8">
            <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 15h2.25m8.024-9.75c.011.05.028.1.052.148.591 1.2.924 2.55.924 3.977a8.96 8.96 0 01-.999 4.125m.023-8.25c-.076-.365.183-.75.575-.75h.908c.889 0 1.713.518 1.972 1.368.339 1.11.521 2.287.521 3.507 0 1.553-.295 3.036-.831 4.398C20.613 14.547 19.833 15 19 15h-1.053c-.472 0-.745-.556-.5-.96a8.95 8.95 0 00.303-.54m.023-8.25H16.48a4.5 4.5 0 01-1.423-.23l-3.114-1.04a4.5 4.5 0 00-1.423-.23H6.504c-.618 0-1.217.247-1.605.729A11.95 11.95 0 002.25 12c0 .434.023.863.068 1.285C2.427 14.306 3.346 15 4.372 15h3.126c.618 0 .991.724.725 1.282A7.471 7.471 0 007.5 19.5a2.25 2.25 0 002.25 2.25.75.75 0 00.75-.75v-.633c0-.573.11-1.14.322-1.672.304-.76.93-1.33 1.653-1.715a9.04 9.04 0 002.86-2.4c.498-.634 1.226-1.08 2.032-1.08h.384" />
          </svg>
          <p class="ml-1">{{ contD }}</p>
        </div>
      </div>

      <div class="flex justify-around bg-slate-200 py-4 rounded-lg">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-w-10">
          <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" />
        </svg>

        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-w-10 bg-slate-100 rounded-lg ">
          <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
        </svg>

        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-10 h-w-10">
          <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
        </svg>

      </div>
    </div>
  </div>
</template>
