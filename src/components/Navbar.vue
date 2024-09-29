<template>
    <header class="flex justify-between items-center p-6 bg-opacity-50 relative z-20">
      <!-- Mobile Toggle Button -->
      <div class="md:hidden z-30">
        <button type="button" 
          class="block focus:outline-none"
          @click="isMenuOpen = !isMenuOpen"
        >
          <span v-if="isMenuOpen" class="text-5xl">
            <img src="https://img.icons8.com/ios-filled/100/ffffff/delete-sign.png" alt="close" width="50" height="50">
          </span>
          <span v-else class="text-5xl">
            <img src="https://img.icons8.com/ios-filled/100/ffffff/menu--v6.png" alt="menu" width="50" height="50">
          </span>
        </button>
      </div>
      <!-- NavBar Links -->
      <nav
        :class="[
          'fixed inset-0 z-20 flex flex-col items-center justify-center bg-[#111827] md:bg-transparent md:flex md:justify-end md:flex-row',
          isMenuOpen ? 'block' : 'hidden'
        ]"
        class="md:static md:flex md:space-x-5"
      >
        <a href="#about" class="block text-white transition hover:text-primary ease-linear text-2xl md:text-lg">About Me</a>
        <a href="#skills" class="block text-white transition hover:text-primary ease-linear text-2xl md:text-lg">Skills</a>
        <a href="#projects" class="block text-white transition hover:text-primary ease-linear text-2xl md:text-lg">Projects</a>
        <a href="#contact" class="block text-white transition hover:text-primary ease-linear text-2xl md:text-lg">Contact Info</a>
      </nav>
    </header>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isMenuOpen = ref(false);
  
  const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section) {
      section.scrollIntoView({ behavior: "smooth" });
    }
  };
  </script>
  