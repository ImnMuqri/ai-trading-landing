<template>
  <header class="fixed h-28 top-0 left-0 w-full z-50 backdrop-blur">
    <nav class="mx-auto px-20 h-20 flex items-end justify-between">
      <p class="text-lg font-bold italic text-white">SIGNALWISE</p>

      <div class="hidden md:flex items-center gap-8 text-sm text-[#BCBBBB]">
        <!-- Home -->
        <NuxtLink
          to="/"
          class="relative group px-1 transition-colors duration-300"
          :class="{ 'text-white': route.path === '/' }">
          Home
          <span
            class="absolute left-0 -bottom-1 w-0 h-[2px] bg-[#3CFFE8] transition-all duration-300"
            :class="{ 'w-full': route.path === '/' }"></span>
        </NuxtLink>

        <!-- Features -->
        <NuxtLink
          to="/features"
          class="relative group px-1 transition-colors duration-300"
          :class="{ 'text-white': route.path === '/features' }">
          Features
          <span
            class="absolute left-0 -bottom-1 w-0 h-[2px] bg-[#3CFFE8] transition-all duration-300"
            :class="{ 'w-full': route.path === '/features' }"></span>
        </NuxtLink>

        <!-- Contact -->
        <NuxtLink
          to="/contact"
          class="relative group px-1 transition-colors duration-300"
          :class="{ 'text-white': route.path === '/contact' }">
          Contact
          <span
            class="absolute left-0 -bottom-1 w-0 h-[2px] bg-[#3CFFE8] transition-all duration-300"
            :class="{ 'w-full': route.path === '/contact' }"></span>
        </NuxtLink>
      </div>

      <a
        href="https://ai-trading-demo-blush.vercel.app/login"
        target="_blank"
        rel="noopener noreferrer"
        class="px-4 text-[#BCBBBB] py-2 text-sm font-medium hover:text-white/80 transition">
        Get Started
      </a>
    </nav>
  </header>
</template>
<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
</script>
