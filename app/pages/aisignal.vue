<template>
  <main class="bg-[#0B071E] background text-white">
    <AISignal id="aisignalengine" />
  </main>
</template>

<script setup>
useSeoMeta({
  title: "AI Engine – Bullise AI Trading Platform",
  description:
    "Learn more about AI trading signals and how we can help you trade smarter.",
  ogTitle: "AI Engine – Bullise AI Trading Platform",
  ogDescription: "Learn the technology behind bullise AI Trading Platform.",
  ogType: "website",
  ogImage: "/AI-Engine-social-preview.png",
  ogUrl: "https://yourdomain.com",
  ogSiteName: "Bullise",
  twitterCard: "summary_large_image",
  twitterSite: "@yourtwitterhandle",
});

useHead({
  script: [
    {
      type: "application/ld+json",
      children: JSON.stringify({
        "@context": "https://schema.org",
        "@type": "WebPage",
        name: "AI Engine – Bullise AI Trading Platform",
        description:
          "Learn more about AI trading signals and how we can help you trade smarter.",
        url: "https://yourdomain.com/aisignal",
        image: "https://yourdomain.com/AI-Engine-social-preview.png",
        publisher: {
          "@type": "Organization",
          name: "Bullise",
          logo: {
            "@type": "ImageObject",
            url: "https://yourdomain.com/logo.png",
          },
        },
      }),
    },
  ],
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
