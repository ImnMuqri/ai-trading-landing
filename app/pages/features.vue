<template>
  <main class="bg-[#0B071E] background text-white">
    <Features id="features" />
  </main>
</template>

<script setup>
useSeoMeta({
  title: "Features – Bullise AI Trading Platform",
  description:
    "Explore the AI trading platform features designed to give traders actionable signals with confidence and risk awareness.",
  ogTitle: "Bullise Features – Bullise AI Trading Platform",
  ogDescription:
    "Discover the AI trading features for smarter trading decisions.",
  ogType: "website",
  ogImage: "/features-social-preview.png",
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
        name: "Features – Bullise AI Trading Platform",
        description:
          "Explore the AI trading platform features designed to give traders actionable signals with confidence and risk awareness.",
        url: "https://yourdomain.com/features",
        image: "https://yourdomain.com/features-social-preview.png",
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
  background-image: url("/Bg2.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
</style>
