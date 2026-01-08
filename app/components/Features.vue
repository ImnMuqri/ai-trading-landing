<template>
  <div class="max-w-6xl mx-auto min-h-screen pt-40 text-center">
    <section id="home" class="md:min-h-[700px] px-10 mx:px-0">
      <p class="text-xl md:text-[30px]">
        Everything You Need to Trade with Confidence
      </p>
      <h1
        class="bg-gradient-to-r from-[#9966FF] to-white bg-clip-text text-transparent font-semibold text-4xl md:text-[90px] leading-tight">
        Tailored Trading Strategies
      </h1>
      <div
        class="mt-0 md:mt-24 flex flex-col justify-center items-center gap-4">
        <div
          class="relative w-full flex flex-col items-center justify-center hidden md:block">
          <div
            class="absolute -top-16 left-1/2 -translate-x-1/2 -z-5 w-full h-[500px] overflow-hidden">
            <NuxtImg
              src="/Screen.svg"
              alt="SignalWise Dashboard"
              class="rounded-lg object-cover h-[700px] w-full" />
            <div
              class="absolute inset-0 rounded-lg"
              style="
                background: linear-gradient(
                  to top,
                  rgba(11, 7, 30, 1) 0%,
                  rgba(11, 7, 30, 0.8) 30%,
                  rgba(11, 7, 30, 0.5) 60%,
                  rgba(11, 7, 30, 0) 100%
                );
              "></div>
          </div>
        </div>
      </div>
    </section>
    <div class="mt-4 md:mt-28 px-10 md:px-0">
      <p class="text-[12px] md:text-lg">
        Leverage sophisticated charting tools and technical analysis features to
        visualize market trends. Our platform provides the necessary instruments
        to analyze price movements and make informed trading decisions.
      </p>
    </div>
    <section id="features" class="mt-12 md:mt-40 px-4 md:px-0">
      <NuxtImg
        src="/AI-signal-feature.svg"
        alt="All SignalWise Features"
        class="rounded-lg object-cover w-full" />
    </section>
    <section
      id="getaccess"
      class="pt-20 md:pt-48 pb-20 px-10 md:px-0 w-full flex flex-col items-center justify-center">
      <div
        class="p-[3px] bg-gradient-to-t from-[#181430] to-[#3CFFE8] w-fit h-fit rounded-full">
        <NuxtLink
          to="/aisignal"
          class="w-fit px-10 py-5 rounded-full bg-gradient-to-r from-[#3CFFE8] to-[#181430] font-medium text-white text-[12px] md:text-lg hover:opacity-90 transition inline-block text-center">
          Access Trade Signals
        </NuxtLink>
      </div>

      <div class="mt-4 text-[12px] md:text-[15px]">
        <p class="font-semibold">No forced trades.</p>
        <p>Signals are generated only when market conditions align.</p>
      </div>
    </section>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
