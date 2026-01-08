<template>
  <main class="bg-[#0B071E] text-white background">
    <Hero id="home" />
  </main>
</template>

<script setup>
useSeoMeta({
  title: "SignalWise AI Trading Platform",
  description: "Automated AI trading platform built for consistent growth.",
  ogTitle: "SignalWise AI Trading Platform",
  ogDescription: "Automated AI trading platform built for consistent growth.",
  ogType: "website",
  ogUrl: "https://yourdomain.com",
  ogSiteName: "SignalWise",
});

useHead({
  link: [{ rel: "canonical", href: "https://yourdomain.com" }],
  script: [
    {
      type: "application/ld+json",
      children: JSON.stringify({
        "@context": "https://schema.org",
        "@type": "SoftwareApplication",
        name: "SignalWise AI Trading Platform",
        operatingSystem: "Web",
        applicationCategory: "FinanceApplication",
        url: "https://yourdomain.com",
        description:
          "Automated AI trading platform built for consistent growth.",
        offers: {
          "@type": "Offer",
          priceCurrency: "USD",
          price: "12.99",
          url: "https://yourdomain.com/signup",
          availability: "https://schema.org/InStock",
        },
      }),
    },
  ],
});
</script>
<style>
.background {
  background-image: url("/Bg1.svg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
