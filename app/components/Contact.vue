<template>
  <div class="pt-32 md:pt-40 pb-20 text-center">
    <div
      class="flex flex-col md:flex-row justify-center items-center md:items-start gap-12">
      <!-- Contact Info -->
      <div class="grid grid-cols-1 gap-4 md:gap-12 text-left px-10 md:px-0">
        <div>
          <h1
            ref="contactTitle"
            class="text-4xl md:text-[80px] leading-tight mb-2">
            Contact Us
          </h1>
          <div ref="contactInfo" class="grid grid-cols-1 text-[12px] gap-2">
            <p>
              Email, call, or complete the form to learn how bullise can help
              your trading journey
            </p>
            <p>support@bullise.com</p>
            <p>111-111-111</p>
          </div>
        </div>

        <!-- Support Cards -->
        <div class="max-w-3xl grid md:grid-cols-3 gap-4">
          <div ref="supportCard1">
            <p class="font-semibold text-md">Customer Support</p>
            <p class="text-[12px] text-gray-300">
              Need help with your account, subscription, or AI signals? Our
              support team is ready to assist you with any technical or
              account-related issues.
            </p>
          </div>

          <div ref="supportCard2">
            <p class="font-semibold text-md">Feedback and Suggestions</p>
            <p class="text-[12px] text-gray-300">
              We value your thoughts. Share your feedback or suggestions to help
              us improve the platform and provide better trading insights.
            </p>
          </div>

          <div ref="supportCard3">
            <p class="font-semibold text-md">Inquiries</p>
            <p class="text-[12px] text-gray-300">
              For business inquiries, partnership opportunities, or general
              questions, reach out to us and our team will respond promptly.
            </p>
          </div>
        </div>
      </div>

      <!-- Contact Form -->
      <div ref="formWrapper">
        <div
          class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF] mx-10 md:mx-0">
          <div
            class="bg-[#0B071E] p-8 rounded-xl h-full text-left px-10 md:px-10">
            <p
              ref="formTitle"
              class="font-semibold text-3xl bg-gradient-to-r from-white to-[#777777] bg-clip-text text-transparent mb-2">
              Get in Touch
            </p>
            <p ref="formDesc" class="text-[12px] mb-6">
              You can reach us anytime and we'll get back to you ASAP
            </p>

            <form ref="formElement" class="flex flex-col gap-4 text-[12px]">
              <div class="flex flex-col md:flex-row gap-4">
                <input
                  type="text"
                  placeholder="First Name"
                  class="flex-1 p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]" />
                <input
                  type="text"
                  placeholder="Last Name"
                  class="flex-1 p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]" />
              </div>

              <input
                type="email"
                placeholder="Email"
                class="w-full p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]" />
              <textarea
                placeholder="How can we help?"
                rows="4"
                class="w-full p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]"></textarea>

              <button
                type="submit"
                class="w-full px-6 py-3 rounded-full bg-[#3CFFE8] text-black font-medium text-sm hover:opacity-90 transition">
                Submit
              </button>
            </form>

            <p ref="formFooter" class="text-[12px] mt-4">
              By contacting us, you agree to our Terms of service and Privacy
              Policy
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

// Refs
const contactTitle = ref(null);
const contactInfo = ref(null);

const supportCard1 = ref(null);
const supportCard2 = ref(null);
const supportCard3 = ref(null);

const formWrapper = ref(null);
const formTitle = ref(null);
const formDesc = ref(null);
const formElement = ref(null);
const formFooter = ref(null);

onMounted(() => {
  if (!process.client) return;

  const animateFrom = (el, delay = 0) => {
    if (!el) return;
    gsap.from(el, {
      y: 50,
      opacity: 0,
      duration: 1,
      delay,
      ease: "power3.out",
      scrollTrigger: {
        trigger: el,
        start: "top 80%",
        toggleActions: "play none none reset",
      },
    });
  };

  // Contact Info
  animateFrom(contactTitle.value);
  animateFrom(contactInfo.value, 0.2);

  // Support Cards
  [supportCard1.value, supportCard2.value, supportCard3.value].forEach(
    (card, i) => animateFrom(card, 0.4 + i * 0.2),
  );

  // Form
  animateFrom(formWrapper.value, 0.6);
  animateFrom(formTitle.value, 0.8);
  animateFrom(formDesc.value, 1);
  animateFrom(formElement.value, 1.2);
  animateFrom(formFooter.value, 1.4);
});
</script>

<style scoped></style>
