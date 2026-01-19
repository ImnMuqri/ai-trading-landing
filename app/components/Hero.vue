<template>
  <div class="grid gap-40 max-w-5xl mx-auto">
    <!-- Home Section -->
    <section
      id="home"
      aria-label="bullise Home Section"
      class="pt-40 md:pt-0 md:min-h-screen flex items-center justify-center px-6">
      <div class="max-w-5xl text-center md:min-h-[650px]">
        <h1
          ref="homeTitle"
          class="md:h-24 text-5xl md:text-[100px] font-semibold leading-tight">
          Execution-Ready
        </h1>

        <h2
          ref="homeSubtitle"
          class="mt-4 md:h-32 text-4xl md:text-[100px] font-semibold leading-tight bg-gradient-to-r from-[#3CFFE8] to-[#FFFFFF] bg-clip-text text-transparent">
          AI Trade Signal
        </h2>

        <p
          ref="homeText"
          class="px-6 md:px-20 mt-4 text-[#FFFFFF] text-base md:text-lg text-center">
          AI-generated buy, sell, or hold signals built from real-time price
          action, volatility, and market conditions, with confidence and risk
          context included.
        </p>

        <div
          ref="homeButtonWrapper"
          class="mt-20 flex flex-col justify-center items-center gap-4">
          <div
            class="relative w-full flex flex-wrap flex-col items-center justify-center">
            <div class="absolute -top-16 left-1/2 -translate-x-1/2 -z-5 w-full">
              <img
                src="/Hero.svg"
                alt="bullise Dashboard"
                class="rounded-lg object-cover h-[600px] w-full hidden md:block" />
              <div
                class="absolute inset-0 rounded-lg"
                style="
                  background: linear-gradient(
                    to top,
                    rgba(11, 7, 30, 1) 0%,
                    rgba(11, 7, 30, 0.8) 50%,
                    rgba(11, 7, 30, 0.5) 80%,
                    rgba(11, 7, 30, 0) 100%
                  );
                "></div>
            </div>

            <button
              ref="homeButton"
              class="z-10 w-fit px-6 py-3 rounded-full bg-[#3CFFE8] font-medium text-black text-sm hover:opacity-90 transition">
              Access Trade Signal
            </button>

            <div class="text-[11px] z-10 text-center mt-2">
              <p class="font-semibold">No forced trades.</p>
              <p>Signals are generated only when market conditions align.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Why Choose Us Section -->
    <section
      id="whychooseus"
      aria-label="Why Choose Us Section"
      class="px-10 md:px-0">
      <p ref="whyTitle" class="md:py-10 text-[18px] text-center md:text-left">
        Why choose Us?
      </p>
      <div class="flex flex-col md:flex-row gap-2 items-start">
        <h2 ref="whySubtitle" class="col-span-1 text-2xl md:text-[52px] mt-4">
          Designed for
        </h2>
        <div class="col-span-2 flex flex-col gap-4 md:gap-8 w-full flex-1">
          <p
            ref="whyText"
            class="text-3xl md:text-[92px] font-bold px-1 leading-tight">
            Real Trading Decisions
          </p>
          <p ref="whyParagraph" class="text-md md:text-[20px] md:w-[500px]">
            Our signal engine focuses on quality, context, and discipline. Every
            trade decision is informed, intentional, and risk-aware.
          </p>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div
              ref="feature1"
              class="border border-[#3CFFE8] p-8 rounded-lg bg-[#3CFFE8] text-black">
              <p class="font-semibold text-md md:text-lg">
                Execution-Ready Trade Signals
              </p>
              <p class="text-sm md:text-md">
                Every signal delivers clear direction. Designed to support real
                trading decisions, not raw analysis.
              </p>
            </div>

            <div
              ref="feature2"
              class="p-[2px] rounded-lg bg-gradient-to-b from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-lg h-full">
                <p class="font-semibold text-md md:text-lg">
                  Confidence-Based Signal Scoring
                </p>
                <p class="text-sm md:text-md">
                  Each signal includes a confidence score, helping you assess
                  strength and conviction before taking action.
                </p>
              </div>
            </div>

            <div
              ref="feature3"
              class="p-[2px] rounded-lg bg-gradient-to-b from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-lg h-full">
                <p class="font-semibold text-md md:text-lg">
                  Market Context, Not Just Direction
                </p>
                <p class="text-sm md:text-md">
                  Signals reflect current market conditions such as trending,
                  ranging, or volatile environments. Understand the context
                  behind every call.
                </p>
              </div>
            </div>

            <div
              ref="feature4"
              class="p-[2px] rounded-lg bg-gradient-to-b from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] rounded-lg p-8 h-full">
                <p class="font-semibold text-md md:text-lg">
                  Risk-Aware by Design
                </p>
                <p class="text-sm md:text-md">
                  Signals are filtered for volatility and news risk, and
                  generated only when conditions align. No forced trades, no
                  unnecessary exposure.
                </p>
              </div>
            </div>
          </div>

          <div
            ref="whyButtonWrapper"
            class="flex flex-col gap-4 md:flex-row items-center justify-center md:justify-between">
            <p class="pr-0 md:pr-10">
              Signals are decision-support tools. Traders retain full control
              over execution and risk management.
            </p>
            <button
              ref="whyButton"
              class="z-10 w-fit whitespace-nowrap px-6 py-3 rounded-full bg-[#3CFFE8] font-medium text-black text-sm hover:opacity-90 transition">
              Access Trade Signal
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section
      id="features"
      class="text-center px-6 md:px-0"
      aria-label="Features Section">
      <h2
        ref="featuresTitle"
        class="text-4xl font-semibold md:font-normal md:text-[100px] leading-tight bg-gradient-to-r from-[#3CFFE8] to-[#FFFFFF] bg-clip-text text-transparent">
        Behind the brilliance
      </h2>

      <p ref="featuresText" class="mt-4">
        The tools that power clarity, speed, and confidence in your decisions.
      </p>

      <div
        ref="featuresSwiper"
        class="relative w-full max-w-sm md:max-w-5xl mx-auto overflow-hidden">
        <ClientOnly>
          <Swiper
            :modules="[Pagination, Autoplay]"
            :slides-per-view="1"
            :space-between="50"
            :autoplay="{ delay: 5000, disableOnInteraction: false }"
            :pagination="{ clickable: true }"
            :observer="true"
            :observe-parents="true"
            :watch-overflow="true"
            class="w-full">
            <!-- Swiper slides omitted for brevity; you can keep your original SwiperSlide content -->
          </Swiper>
        </ClientOnly>
      </div>
    </section>

    <!-- Pricing Section -->
    <section
      id="pricing"
      aria-label="Pricing Section"
      class="text-center px-10 lg:px-0">
      <h2
        ref="pricingTitle"
        class="text-3xl md:text-[90px] leading-tight tex-white">
        Plans that fit your strategy
      </h2>
      <div class="mt-12 flex flex-wrap justify-around gap-6 h-[450px]">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
          <div
            v-for="(pkg, i) in subscriptionPackages"
            :key="pkg.name"
            :ref="(el) => (pricingCards[i] = el)"
            class="p-[2px] rounded-xl"
            :class="[
              pkg.name == 'Pro'
                ? 'bg-gradient-to-t from-[#00000000] to-[#3CFFE8]'
                : 'bg-gradient-to-t from-[#0B071E] to-[#9966FF]',
            ]">
            <div
              class="flex flex-col justify-between text-left p-8 rounded-xl h-full"
              :class="[
                pkg.name == 'Pro'
                  ? 'bg-gradient-to-br from-[#0B071E] to-[#3CFFE8]/30'
                  : 'bg-gradient-to-br from-[#0B071E] to-[#9966FF]/30',
              ]">
              <div>
                <p
                  class="bg-gradient-to-r from-[#FFFFFF] to-[#777777] bg-clip-text text-transparent font-bold">
                  {{ pkg.name }}
                </p>
                <div class="flex font-semibold mt-2">
                  <p class="text-5xl lg:text-7xl">
                    ${{ Math.floor(pkg.price) }}
                  </p>
                  <div class="flex flex-col gap-1 items-start justify-end">
                    <p class="text-2xl lg:text-4xl">
                      .{{ pkg.price.toFixed(2).split(".")[1] }}
                    </p>
                    <p class="font-normal text-gray-400">{{ pkg.period }}</p>
                  </div>
                </div>
                <div class="py-6 text-[12px] sm:text-md space-y-2">
                  <div
                    v-for="(feature, index) in pkg.features"
                    :key="index"
                    class="flex items-start gap-2">
                    <Icon
                      name="mdi:check-circle"
                      class="text-emerald-400 text-sm mt-[2px]" />
                    <span>{{ feature }}</span>
                  </div>
                </div>
              </div>

              <div
                class="p-[2px] rounded-full w-full"
                :class="[
                  pkg.name == 'Pro'
                    ? 'bg-gradient-to-t from-[#181430] to-[#3CFFE8]'
                    : 'bg-gradient-to-t from-[#181430] to-[#4B3F96]',
                ]">
                <button
                  class="z-10 w-full px-8 py-3 rounded-full font-medium text-white text-[12px] lg:text-sm hover:opacity-90 transition"
                  :class="[
                    pkg.name == 'Pro'
                      ? 'bg-gradient-to-r  from-[#3CFFE8] to-[#181430]'
                      : 'bg-gradient-to-r from-[#9966FF] to-[#181430]',
                  ]">
                  {{
                    pkg.name === "Basic" ? "Get Started" : "Unlock Pro Access"
                  }}
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section
      id="contact"
      class="text-center pt-[500px] md:pt-0 mb-20 px-10 lg:px-0">
      <h2
        ref="contactTitle"
        class="text-2xl md:text-[80px] font-light leading-tight text-white">
        Want to Know More?
      </h2>
      <p
        ref="contactSubtitle"
        class="text-xl md:text-[100px] leading-tight font-bold">
        Let Us Show You
      </p>
      <button
        ref="contactButton"
        class="mt-12 w-fit px-8 py-3 rounded-full bg-[#3CFFE8] font-medium text-black text-sm hover:opacity-90 transition">
        Access Trade Signals
      </button>
    </section>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination, Autoplay } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

gsap.registerPlugin(ScrollTrigger);

// Subscription Packages
const subscriptionPackages = [
  {
    name: "Basic",
    price: 15,
    period: "/month",
    billedAnnually: "Billed annually at $155.88/year",
    features: [
      "Up to 5 AI signal requests per day",
      "Personalized AI market intelligence",
      "Live market sentiment and trend indicators",
      "Real time financial news and headlines",
      "AI curated economic events calendar",
      "Global market overview dashboards",
      "Professional grade equity research",
    ],
  },
  {
    name: "Pro",
    price: 30,
    period: "/month",
    billedAnnually: "Billed annually at $354.00/year",
    features: [
      "Up to 15 AI signal requests per day",
      "Personalized AI market intelligence",
      "Live market sentiment and trend indicators",
      "Real time financial news and headlines",
      "AI curated economic events calendar",
      "Global market overview dashboards",
      "Professional grade equity research",
    ],
  },
];

// Refs for sections
const homeTitle = ref(null);
const homeSubtitle = ref(null);
const homeText = ref(null);
const homeButtonWrapper = ref(null);

const whyTitle = ref(null);
const whySubtitle = ref(null);
const whyText = ref(null);
const whyParagraph = ref(null);
const whyButtonWrapper = ref(null);

const feature1 = ref(null);
const feature2 = ref(null);
const feature3 = ref(null);
const feature4 = ref(null);

const featuresTitle = ref(null);
const featuresText = ref(null);
const featuresSwiper = ref(null);

const pricingTitle = ref(null);
const pricingCards = [];

const contactTitle = ref(null);
const contactSubtitle = ref(null);
const contactButton = ref(null);

onMounted(() => {
  if (process.client) {
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

    // Home Animations
    animateFrom(homeTitle.value);
    animateFrom(homeSubtitle.value, 0.2);
    animateFrom(homeText.value, 0.4);
    animateFrom(homeButtonWrapper.value, 0.6);

    // Why Choose Us Animations
    gsap.from(
      [whyTitle.value, whySubtitle.value, whyText.value, whyParagraph.value],
      {
        y: 50,
        opacity: 0,
        duration: 1,
        ease: "power3.out",
        stagger: 0.2,
        scrollTrigger: {
          trigger: whyTitle.value,
          start: "top 80%",
          toggleActions: "play pause resume reset",
        },
      },
    );
    animateFrom(whyButtonWrapper.value);

    // Feature Cards
    [feature1.value, feature2.value, feature3.value, feature4.value].forEach(
      (f, i) => {
        animateFrom(f, i * 0.2);
      },
    );

    // Features Section
    animateFrom(featuresTitle.value);
    animateFrom(featuresText.value);
    animateFrom(featuresSwiper.value);

    // Pricing Section
    animateFrom(pricingTitle.value);
    pricingCards.forEach((card, i) => {
      if (card) animateFrom(card, i * 0.2);
    });

    // Contact Section
    animateFrom(contactTitle.value);
    animateFrom(contactSubtitle.value, 0.2);
    animateFrom(contactButton.value, 0.4);
  }
});
</script>
