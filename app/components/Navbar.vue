<template>
  <header class="fixed top-0 left-0 w-full z-50 backdrop-blur h-20">
    <nav
      class="mx-auto px-6 md:px-20 h-20 flex items-center justify-between relative">
      <!-- Logo -->
      <img
        src="/BulliseLogo.svg"
        alt="Bullise Logo"
        class="rounded-lg h-full w-[150px]" />

      <!-- Desktop Links -->
      <div class="hidden md:flex items-center gap-8 text-sm text-[#BCBBBB]">
        <NuxtLink
          to="/"
          class="relative group px-1 transition-colors duration-300"
          :class="{ 'text-white': route.path === '/' }">
          Home
          <span
            class="absolute left-0 -bottom-1 w-0 h-[2px] bg-[#3CFFE8] transition-all duration-300"
            :class="{ 'w-full': route.path === '/' }"></span>
        </NuxtLink>

        <NuxtLink
          to="/features"
          class="relative group px-1 transition-colors duration-300"
          :class="{ 'text-white': route.path === '/features' }">
          Features
          <span
            class="absolute left-0 -bottom-1 w-0 h-[2px] bg-[#3CFFE8] transition-all duration-300"
            :class="{ 'w-full': route.path === '/features' }"></span>
        </NuxtLink>

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

      <!-- Get Started Button -->
      <a
        href="https://ai-trading-demo-blush.vercel.app/login"
        target="_blank"
        rel="noopener noreferrer"
        class="px-4 text-[#BCBBBB] py-2 text-sm font-medium hover:text-white/80 transition max-[380px]:hidden">
        Get Started
      </a>

      <!-- Mobile Burger -->
      <button
        class="md:hidden flex flex-col justify-center items-center gap-1 w-8 h-8 relative z-50"
        @click="toggleMobileMenu"
        aria-label="Toggle Mobile Menu">
        <span
          :class="[
            'block w-5 h-0.5 bg-white transition-all duration-300',
            mobileMenuOpen ? 'rotate-45 translate-y-2 ' : '',
          ]"></span>
        <span
          :class="[
            'block w-5 h-0.5 bg-white transition-all duration-300',
            mobileMenuOpen ? 'opacity-0' : '',
          ]"></span>
        <span
          :class="[
            'block w-5 h-0.5 bg-white transition-all duration-300',
            mobileMenuOpen ? '-rotate-45 -translate-y-1' : '',
          ]"></span>
      </button>

      <!-- Mobile Menu Overlay -->
      <transition name="fade">
        <div
          v-if="mobileMenuOpen"
          class="fixed inset-0 bg-black/60 backdrop-blur-sm z-40"
          @click="toggleMobileMenu"></div>
      </transition>

      <!-- Mobile Menu -->
      <transition name="slide-down">
        <div
          v-if="mobileMenuOpen"
          class="fixed top-20 left-0 w-full bg-[#1A1C20] z-50 flex flex-col items-center py-6 gap-6">
          <NuxtLink
            to="/"
            class="text-white text-sm font-medium"
            @click="toggleMobileMenu">
            Home
          </NuxtLink>
          <NuxtLink
            to="/features"
            class="text-white text-sm font-medium"
            @click="toggleMobileMenu">
            Features
          </NuxtLink>
          <NuxtLink
            to="/contact"
            class="text-white text-sm font-medium"
            @click="toggleMobileMenu">
            Contact
          </NuxtLink>
          <a
            href="https://ai-trading-demo-blush.vercel.app/login"
            target="_blank"
            rel="noopener noreferrer"
            class="px-6 py-2 bg-[#00BDA7] rounded-full text-black font-medium text-sm">
            Get Started
          </a>
        </div>
      </transition>
    </nav>
  </header>
</template>

<script setup>
import { ref, watch } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const mobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};

// Lock scroll when menu is open
watch(mobileMenuOpen, (isOpen) => {
  if (isOpen) document.body.classList.add("overflow-hidden");
  else document.body.classList.remove("overflow-hidden");
});
</script>

<style>
/* Animations */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.slide-down-enter-active {
  transition: transform 0.3s ease, opacity 0.3s ease;
}
.slide-down-enter-from {
  transform: translateY(-20px);
  opacity: 0;
}
.slide-down-enter-to {
  transform: translateY(0);
  opacity: 1;
}
.slide-down-leave-active {
  transition: transform 0.2s ease, opacity 0.2s ease;
}
.slide-down-leave-to {
  transform: translateY(-20px);
  opacity: 0;
}
</style>
