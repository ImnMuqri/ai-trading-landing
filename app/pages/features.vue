<template>
  <main class="bg-[#0B071E] background text-white">
    <Features id="features" />
  </main>
</template>

<script setup>
useSeoMeta({
  title: "Features – SignalWise AI Trading Platform",
  description:
    "Explore the AI trading platform features designed to give traders actionable signals with confidence and risk awareness.",
  ogTitle: "SignalWise Features – SignalWise AI Trading Platform",
  ogDescription:
    "Discover the AI trading features for smarter trading decisions.",
  ogType: "website",
  ogImage: "/features-social-preview.png",
  ogUrl: "https://yourdomain.com",
  ogSiteName: "SignalWise",
  twitterCard: "summary_large_image",
  twitterSite: "@yourtwitterhandle",
});

useHead({
  link: [{ rel: "canonical", href: "https://yourdomain.com/features" }],
});
</script>

<style scoped>
.background {
  background-image: url("/Bg2.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
</style>
