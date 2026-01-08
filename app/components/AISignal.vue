<template>
  <div class="min-h-screen pt-40 text-center">
    <div class="max-w-6xl mx-auto">
      <div class="grid gap-40 min-h-screen">
        <div id="home" class="mt-10">
          <h1
            class="bg-gradient-to-r from-[#3CFFE8] to-white bg-clip-text text-transparent font-semibold text-[90px] leading-tight">
            AI Signals Engine
          </h1>
          <p class="text-[40px]">From Market Noise to Trade Signal</p>
          <h2 class="text-lg px-40">
            Transform unstructured market data into deterministic trade signals.
            The AI Signal Engine executes “From noise to certainty”, applying
            rigorous machine learning to distill high-frequency inputs into
            validated, risk-adjusted outputs for global asset classes.
          </h2>
          <div class="mt-28">
            <button
              class="z-10 w-fit px-6 py-3 rounded-full bg-[#3CFFE8] font-medium text-black text-sm hover:opacity-90 transition">
              Access Trade Signal
            </button>

            <!-- Text -->
            <div class="text-[11px] z-10 text-center mt-2">
              <p class="text-[12px] font-semibold">No forced trades.</p>
              <p>Signals are generated only when market conditions align.</p>
            </div>
          </div>
        </div>
        <div id="features">
          <div class="flex items-center justify-center gap-4 text-[#3CFFE8]">
            <p>Market Inputs</p>
            <span class="h-4 border border-[#3CFFE8]"></span>
            <p>Capturing the full picture</p>
          </div>
          <p class="text-[40px] mb-4">
            We ingest real-time data streams to build a comprehensive view of
            market dynamics
          </p>
          <div class="grid grid-cols-3 gap-6 text-left mt-20">
            <div
              class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-xl h-full">
                <p
                  class="font-semibold text-3xl bg-gradient-to-r from-white to[#777777] bg-clip-text text-transparent mb-6">
                  News
                </p>
                <p>
                  Sentiment analysis from global headlines, earnings reports,
                  and economic events.
                </p>
              </div>
            </div>
            <div
              class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-xl h-full">
                <p
                  class="font-semibold text-3xl bg-gradient-to-r from-white to[#777777] bg-clip-text text-transparent mb-6">
                  Price Action
                </p>
                <p>Patterns, trends, and momentum across assets.</p>
              </div>
            </div>
            <div
              class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF]">
              <div class="bg-[#0B071E] p-8 rounded-xl h-full">
                <p
                  class="font-semibold text-3xl bg-gradient-to-r from-white to[#777777] bg-clip-text text-transparent mb-6">
                  Volatility
                </p>
                <p>
                  Measures like VIX, implied vols, and sudden spikes for risk
                  context.
                </p>
              </div>
            </div>
          </div>
          <p class="py-20">
            No detail is overlooked, every input fuels smarter decisions.
          </p>
        </div>
        <div id="signal" aria-label="SignalWise Ai Features">
          <div class="flex items-center justify-center gap-4 text-[#3CFFE8]">
            <p>AI Signal Processing</p>
            <span class="h-4 border border-[#3CFFE8]"></span>
            <p>Precision in Every Step</p>
          </div>
          <h2
            class="px-10 bg-gradient-to-r from-[#3CFFE8] to-white bg-clip-text text-transparent font-semibold text-[90px] leading-tight">
            Advanced AI Algorithms
          </h2>
          <p class="text-[50px]">refine the noise into crystal-clear signals</p>
          <div class="mt-40">
            <NuxtImg
              src="/AI-signal-processing.svg"
              alt="All SignalWise Features"
              class="rounded-lg object-cover w-full" />
            <div class="px-40">
              <div
                class="p-[2px] rounded-full bg-gradient-to-b from-[#0B071E] to-[#9966FF]">
                <div class="bg-[#0B071E] p-8 rounded-full h-full">
                  <p>
                    This multi-layer process ensures only the strongest signals
                    emerge, backed by machine learning trained on decades of
                    market history.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="outputs" aria-label="SignalWise Trade Outputs">
          <div class="flex items-center justify-center gap-4 text-[#3CFFE8]">
            <p>Trade Outputs</p>
            <span class="h-4 border border-[#3CFFE8]"></span>
            <p>Ready-to-Act Intelligence</p>
          </div>

          <p class="text-[40px]">
            Get instant, executable insights tailored for your strategy
          </p>
          <div class="mt-10">
            <NuxtImg
              src="/Trade-outputs.svg"
              alt="All SignalWise Features"
              class="rounded-lg object-cover w-full" />
          </div>
        </div>
        <div
          id="access"
          aria-label="Get Access"
          class="py-40 w-full flex flex-col items-center justify-center">
          <div class="mb-6">
            <p class="text-[80px]">From noise to certainty</p>
            <p class="text-[40px]">Empower your trades with signals that win</p>
          </div>
          <div
            class="p-[3px] bg-gradient-to-t from-[#181430] to-[#3CFFE8] w-fit h-fit rounded-full">
            <NuxtLink
              to="/aisignal"
              class="w-fit px-10 py-5 rounded-full bg-gradient-to-r from-[#3CFFE8] to-[#181430] font-medium text-white text-lg hover:opacity-90 transition inline-block text-center">
              Access Trade Signals
            </NuxtLink>
          </div>

          <div class="mt-4 text-[15px]">
            <p>No forced trades.</p>
            <p>Signals are generated only when market conditions align.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
