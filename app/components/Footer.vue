<template>
  <footer
    class="text-white px-6 md:px-0 pt-[20vh] md:pt-40"
    :class="[
      route.name === 'features'
        ? 'bg-gradient-to-t from-[#008E7E] to-[#0B071E]'
        : route.name === 'aisignal'
        ? 'bg-gradient-to-t from-[#9966FF] to-[#0B071E]'
        : 'bg-[#0B071E]',
    ]">
    <div class="max-w-7xl mx-auto text-center text-[12px] text-white">
      SignalWise provides analytical information and market signals for
      informational purposes only. It does not constitute financial, investment,
      trading, or legal advice, nor an offer or solicitation to buy or sell any
      financial instrument. Users should conduct their own research and consult
      qualified professionals before making any investment decisions.
    </div>
    <div class="max-w-7xl mx-auto px-6 py-12 grid md:grid-cols-6 gap-8">
      <!-- Logo / Branding -->
      <div class="col-span-2">
        <h2 class="text-white font-bold italic text-xl mb-2">SIGNALWISE</h2>
        <p class="text-sm">
          TrueProTech delivers smart, real-time risk management and monitoring
          tools for brokerages.
        </p>
      </div>

      <!-- Navigation -->
      <div>
        <h3 class="text-white font-semibold mb-2">Site Map</h3>
        <ul class="space-y-2 text-[12px]">
          <li>
            <a
              href="#home"
              @click.prevent="scrollToSection('home')"
              :class="{ 'text-white': activeSection === 'home' }"
              class="hover:text-white transition">
              Home
            </a>
          </li>
          <li>
            <a
              href="#whychooseus"
              @click.prevent="scrollToSection('whychooseus')"
              :class="{ 'text-white': activeSection === 'whychooseus' }"
              class="hover:text-white transition">
              Why Choose Us
            </a>
          </li>
          <li>
            <a
              href="#features"
              @click.prevent="scrollToSection('features')"
              :class="{ 'text-white': activeSection === 'features' }"
              class="hover:text-white transition">
              Features
            </a>
          </li>
          <li>
            <a
              href="#pricing"
              @click.prevent="scrollToSection('pricing')"
              :class="{ 'text-white': activeSection === 'pricing' }"
              class="hover:text-white transition">
              Pricing
            </a>
          </li>
          <li>
            <a
              href="#contact"
              @click.prevent="scrollToSection('contact')"
              :class="{ 'text-white': activeSection === 'contact' }"
              class="hover:text-white transition">
              Contact
            </a>
          </li>
        </ul>
      </div>

      <!-- Address -->
      <div>
        <h3 class="text-white font-semibold mb-2">Company Address</h3>
        <p class="text-[12px]">
          Addiyar Building, Sheikh Zayed Rd, Al Wasl, Dubai, United Arab
          Emirates
        </p>
      </div>

      <!-- Social / Contact -->
      <div>
        <h3 class="text-white font-semibold mb-2">Contact Us</h3>
        <p class="text-[12px]">support@signalwise.com</p>
      </div>
      <div>
        <h3 class="text-white font-semibold mb-2">Legal</h3>
        <p class="text-[12px]">Privacy Policy</p>
        <p class="text-[12px]">Terms of Use</p>
      </div>
    </div>

    <div
      class="border-t border-white mt-8 py-4 mx-[5%] text-center text-gray-500 text-[15px] text-white">
      &copy; {{ new Date().getFullYear() }} SignalWise. All rights reserved.
    </div>
  </footer>
</template>
<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const activeSection = ref("home");

// IDs of the sections
const sections = [
  { id: "home", label: "Home" },
  { id: "whychooseus", label: "Why Choose Us" },
  { id: "features", label: "Features" },
  { id: "pricing", label: "Pricing" },
  { id: "contact", label: "Contact" },
];

const SCROLL_OFFSET = 120; // adjust this for your navbar / hero spacing
const handleScroll = () => {
  const scrollY = window.scrollY + SCROLL_OFFSET;

  for (let i = sections.length - 1; i >= 0; i--) {
    const el = document.getElementById(sections[i].id);
    if (el && scrollY >= el.offsetTop) {
      activeSection.value = sections[i].id;
      break;
    }
  }
};

const scrollToSection = (id) => {
  const el = document.getElementById(id);
  if (el) {
    const y = el.getBoundingClientRect().top + window.scrollY - SCROLL_OFFSET;
    window.scrollTo({ top: y, behavior: "smooth" });
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>
