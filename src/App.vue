<template>
  <div class="text-gray-600 font-body grid md:grid-cols-3">
    <div class="md:col-span-1 md:flex md:justify-end">
      <nav class="text-right">
        <div class="flex justify-between items-center border-b border-gray-100">
          <h1 class="font-bold uppercase p-4 text-mammoth">
            <router-link to="/" class="hover:text-gray-700"
              >Food Ninja</router-link
            >
          </h1>
          <div
            class="px-4 cursor-pointer md:hidden"
            @click="isMenuOpen = !isMenuOpen"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
          </div>
        </div>
        <the-menu :isMenuOpen="isMenuOpen" />
      </nav>
    </div>
    <main class="md:px-16 px-4 py-6 bg-gray-100 md:col-span-2 min-h-screen">
      <div class="flex justify-center md:justify-end">
        <a
          href="#"
          class="btn text-primary md:border-2 border-primary hover:bg-primary hover:text-white transition-all ease-out duration-500"
          >Log in</a
        >
        <a
          href="#"
          class="btn text-primary md:border-2 border-primary ml-2 hover:bg-primary hover:text-white transition-all ease-out duration-500"
          >Sign up</a
        >
      </div>
      <router-view />
    </main>
  </div>
</template>

<script setup>
import TheMenu from "./components/TheMenu.vue";
import { ref } from "vue";
const isMenuOpen = ref(false);
</script>
