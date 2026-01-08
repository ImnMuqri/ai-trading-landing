<template>
  <div class="fixed bottom-8 right-8 z-50 flex flex-col items-center gap-4">
    <!-- Section Indicator -->
    <transition name="column-pop">
      <div
        v-if="sections.length && visible"
        class="flex flex-col gap-3 items-center">
        <span
          v-for="section in sections"
          :key="section.id"
          class="w-2 h-2 rounded-full transition-all duration-300 relative"
          :class="
            activeSection === section.id
              ? 'bg-[#3CFFE8] scale-125'
              : 'bg-white/30'
          ">
          <transition name="fade">
            <p
              v-if="isScrolling && activeSection === section.id"
              class="absolute -left-2 -translate-x-full -top-1 text-[10px] text-[#3CFFE8] capitalize whitespace-nowrap">
              {{ section.label }}
            </p>
          </transition>
        </span>
      </div>
    </transition>

    <transition name="column-pop">
      <button
        v-show="visible"
        @click="scrollToTop"
        class="h-8 w-8 rounded-full bg-[#3CFFE8] text-black shadow-lg hover:opacity-90 transition">
        ↑
      </button>
    </transition>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount, watch, nextTick } from "vue";
import { useRoute } from "vue-router";

const visible = ref(false);
const activeSection = ref("");
const isScrolling = ref(false);
const sections = ref([]);
let scrollTimeout;

const SCROLL_OFFSET = 200; // tweak this for padding/margin corrections
const route = useRoute();

/**
 * Update sections based on what exists in the DOM.
 * Use nextTick to ensure DOM is rendered.
 */
const updateSections = async () => {
  await nextTick();

  const allSections = [
    { id: "home", label: "Home" },
    { id: "whychooseus", label: "Why Choose Us" },
    { id: "features", label: "Features" },
    { id: "pricing", label: "Pricing" },
    { id: "contact", label: "Contact" },
    { id: "signal", label: "How it works" },
    { id: "outputs", label: "What you get" },
    { id: "access", label: "Get Access" },
  ];

  // Filter only sections actually in DOM
  sections.value = allSections.filter((s) => document.getElementById(s.id));

  // Default to first section if available
  if (sections.value.length) {
    activeSection.value = sections.value[0].id;
  }
};

/**
 * Detect scroll and update active section
 */
const onScroll = () => {
  const scrollY = window.scrollY + SCROLL_OFFSET;
  visible.value = window.scrollY > 400;
  isScrolling.value = true;

  // Iterate through sections to find the last section the scroll passed
  for (let i = sections.value.length - 1; i >= 0; i--) {
    const el = document.getElementById(sections.value[i].id);
    if (el && scrollY >= el.offsetTop) {
      activeSection.value = sections.value[i].id;
      break;
    }
  }

  clearTimeout(scrollTimeout);
  scrollTimeout = setTimeout(() => {
    isScrolling.value = false;
  }, 800);
};

/**
 * Scroll to top button
 */
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};

// Initialize
onMounted(() => {
  updateSections();
  window.addEventListener("scroll", onScroll);
});

// Recompute sections when navigating to a new page
watch(
  () => route.fullPath,
  () => {
    setTimeout(updateSections, 50); // give DOM a moment to render
  }
);

onBeforeUnmount(() => {
  window.removeEventListener("scroll", onScroll);
});
</script>

<style scoped>
/* Pop-in transition for the entire column */
.column-pop-enter-active {
  transition: transform 0.3s ease, opacity 0.3s ease;
}
.column-pop-leave-active {
  transition: transform 0.2s ease, opacity 0.2s ease;
}
.column-pop-enter-from {
  transform: scale(0.5);
  opacity: 0;
}
.column-pop-enter-to {
  transform: scale(1);
  opacity: 1;
}
.column-pop-leave-from {
  transform: scale(1);
  opacity: 1;
}
.column-pop-leave-to {
  transform: scale(0.5);
  opacity: 0;
}

/* Label fade */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
