<template>
  <main class="bg-[#0B071E] background text-white">
    <AISignal id="aisignalengine" />
  </main>
</template>

<script setup>
useSeoMeta({
  title: "AI Engine – SignalWise AI Trading Platform",
  description:
    "Learn more about AI trading signals and how we can help you trade smarter.",
  ogTitle: "AI Engine – SignalWise AI Trading Platform",
  ogDescription: "Learn the technology behind SignalWise AI Trading Platform.",
  ogType: "website",
  ogImage: "/AI-Engine-social-preview.png",
  ogUrl: "https://yourdomain.com",
  ogSiteName: "SignalWise",
  twitterCard: "summary_large_image",
  twitterSite: "@yourtwitterhandle",
});

useHead({
  link: [{ rel: "canonical", href: "https://yourdomain.com/aisignal" }],
});
</script>

<style scoped>
.background {
  background-image: url("/Bg3.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
}
</style>
