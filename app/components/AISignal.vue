<template>
  <div class="min-h-screen pt-40 text-center px-10 md:px-0">
    <div class="max-w-6xl mx-auto">
      <div class="grid gap-40 min-h-screen">
        <!-- Home Section -->
        <div id="home">
          <h1
            ref="homeTitle"
            class="bg-gradient-to-r from-[#3CFFE8] to-white bg-clip-text text-transparent font-semibold text-3xl md:text-[90px] leading-tight">
            AI Signals Engine
          </h1>
          <p ref="homeSubtitle" class="text-xl md:text-[40px] leading-tight">
            From Market Noise to Trade Signal
          </p>
          <h2 ref="homeText" class="text-sm md:text-lg md:px-40 mt-4">
            Transform unstructured market data into deterministic trade signals.
            The AI Signal Engine executes “From noise to certainty”, applying
            rigorous machine learning to distill high-frequency inputs into
            validated, risk-adjusted outputs for global asset classes.
          </h2>
          <div ref="homeButtonWrapper" class="mt-28">
            <button
              class="z-10 w-fit px-6 py-3 rounded-full bg-[#3CFFE8] font-medium text-black text-sm hover:opacity-90 transition">
              Access Trade Signal
            </button>

            <div class="text-[11px] z-10 text-center mt-2">
              <p class="text-[12px] font-semibold">No forced trades.</p>
              <p>Signals are generated only when market conditions align.</p>
            </div>
          </div>
        </div>

        <!-- Features Section -->
        <div id="features">
          <div
            ref="featuresHeader"
            class="flex items-center justify-center gap-4 text-[#3CFFE8] text-[12px] md:text-sm">
            <p>Market Inputs</p>
            <span class="h-4 border border-[#3CFFE8]"></span>
            <p>Capturing the full picture</p>
          </div>
          <p
            ref="featuresText"
            class="text-xl md:text-[40px] leading-tight mt-4">
            We ingest real-time data streams to build a comprehensive view of
            market dynamics
          </p>

          <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-left mt-20">
            <div
              ref="featureCard1"
              class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-xl h-full">
                <p
                  class="font-semibold text-xl md:text-3xl bg-gradient-to-r from-white to-[#777777] bg-clip-text text-transparent mb-6">
                  News
                </p>
                <p>
                  Sentiment analysis from global headlines, earnings reports,
                  and economic events.
                </p>
              </div>
            </div>
            <div
              ref="featureCard2"
              class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-xl h-full">
                <p
                  class="font-semibold text-xl md:text-3xl bg-gradient-to-r from-white to-[#777777] bg-clip-text text-transparent mb-6">
                  Price Action
                </p>
                <p>Patterns, trends, and momentum across assets.</p>
              </div>
            </div>
            <div
              ref="featureCard3"
              class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-xl h-full">
                <p
                  class="font-semibold text-xl md:text-3xl bg-gradient-to-r from-white to-[#777777] bg-clip-text text-transparent mb-6">
                  Volatility
                </p>
                <p>
                  Measures like VIX, implied vols, and sudden spikes for risk
                  context.
                </p>
              </div>
            </div>
          </div>
          <p ref="featuresFooter" class="py-20">
            No detail is overlooked, every input fuels smarter decisions.
          </p>
        </div>

        <!-- Signal Section -->
        <div id="signal" aria-label="bullise Ai Features">
          <div
            ref="signalHeader"
            class="flex items-center justify-center gap-4 text-[#3CFFE8] text-[12px] md:text-sm">
            <p>AI Signal Processing</p>
            <span class="h-4 border border-[#3CFFE8]"></span>
            <p>Precision in Every Step</p>
          </div>
          <h2
            ref="signalTitle"
            class="px-10 bg-gradient-to-r from-[#3CFFE8] to-white bg-clip-text text-transparent font-semibold text-3xl md:text-[90px] leading-tight">
            Advanced AI Algorithms
          </h2>
          <p ref="signalText" class="text-xl md:text-[50px] mt-4">
            refine the noise into crystal-clear signals
          </p>
          <div ref="signalImageWrapper" class="mt-10 md:mt-40">
            <img
              src="/Ai-signal-processing.svg"
              alt="All bullise Features"
              class="rounded-lg w-full" />
            <div class="md:px-40 mt-6">
              <div
                class="p-[2px] rounded-full bg-gradient-to-b from-[#0B071E] to-[#9966FF]">
                <div class="bg-[#0B071E] p-8 rounded-full h-full">
                  <p class="text-[12px] md:text-lg">
                    This multi-layer process ensures only the strongest signals
                    emerge, backed by machine learning trained on decades of
                    market history.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Outputs Section -->
        <div id="outputs" aria-label="bullise Trade Outputs">
          <div
            ref="outputsHeader"
            class="flex items-center justify-center gap-4 text-[#3CFFE8] text-[12px] md:text-sm">
            <p>Trade Outputs</p>
            <span class="h-4 border border-[#3CFFE8]"></span>
            <p>Ready-to-Act Intelligence</p>
          </div>
          <p
            ref="outputsText"
            class="text-xl md:text-[40px] leading-tight mt-4">
            Get instant, executable insights tailored for your strategy
          </p>
          <div ref="outputsImageWrapper" class="mt-10">
            <img
              src="/Trade-outputs.svg"
              alt="All bullise Features"
              class="rounded-lg object-cover h-full w-full" />
          </div>
        </div>

        <!-- Access Section -->
        <div
          id="access"
          aria-label="Get Access"
          class="pb-20 md:py-40 w-full flex flex-col items-center justify-center">
          <div ref="accessTitleWrapper" class="mb-6">
            <p class="text-3xl md:text-[80px]">From noise to certainty</p>
            <p class="text-xl md:text-[40px] mt-4 leading-tight">
              Empower your trades with signals that win
            </p>
          </div>
          <div
            ref="accessButtonWrapper"
            class="p-[3px] bg-gradient-to-t from-[#181430] to-[#3CFFE8] w-fit h-fit rounded-full">
            <NuxtLink
              to="/aisignal"
              class="w-fit px-10 py-5 rounded-full bg-gradient-to-r from-[#3CFFE8] to-[#181430] font-medium text-white text-sm md:text-lg hover:opacity-90 transition inline-block text-center">
              Access Trade Signals
            </NuxtLink>
          </div>

          <div ref="accessText" class="mt-4 text-[15px]">
            <p class="font-semibold">No forced trades.</p>
            <p>Signals are generated only when market conditions align.</p>
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
const homeTitle = ref(null);
const homeSubtitle = ref(null);
const homeText = ref(null);
const homeButtonWrapper = ref(null);

const featuresHeader = ref(null);
const featuresText = ref(null);
const featureCard1 = ref(null);
const featureCard2 = ref(null);
const featureCard3 = ref(null);
const featuresFooter = ref(null);

const signalHeader = ref(null);
const signalTitle = ref(null);
const signalText = ref(null);
const signalImageWrapper = ref(null);

const outputsHeader = ref(null);
const outputsText = ref(null);
const outputsImageWrapper = ref(null);

const accessTitleWrapper = ref(null);
const accessButtonWrapper = ref(null);
const accessText = ref(null);

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

  // Home
  animateFrom(homeSubtitle.value);
  animateFrom(homeTitle.value, 0.2);
  animateFrom(homeText.value, 0.4);
  animateFrom(homeButtonWrapper.value, 0.6);

  // Features
  animateFrom(featuresHeader.value);
  animateFrom(featuresText.value, 0.2);
  [featureCard1.value, featureCard2.value, featureCard3.value].forEach(
    (card, i) => animateFrom(card, 0.4 + i * 0.2),
  );
  animateFrom(featuresFooter.value, 1);

  // Signal Section
  animateFrom(signalHeader.value);
  animateFrom(signalTitle.value, 0.2);
  animateFrom(signalText.value, 0.4);
  animateFrom(signalImageWrapper.value, 0.6);

  // Outputs Section
  animateFrom(outputsHeader.value);
  animateFrom(outputsText.value, 0.2);
  animateFrom(outputsImageWrapper.value, 0.4);

  // Access Section
  animateFrom(accessTitleWrapper.value);
  animateFrom(accessButtonWrapper.value, 0.2);
  animateFrom(accessText.value, 0.4);
});
</script>

<style scoped></style>
