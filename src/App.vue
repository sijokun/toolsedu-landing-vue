<script setup>
import { ref } from 'vue'
import LandingNav from './components/LandingNav.vue'
import HeroSection from './components/HeroSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import HowItWorks from './components/HowItWorks.vue'
import TestimonialSection from './components/TestimonialSection.vue'
import PricingSection from './components/PricingSection.vue'
import MissionSection from './components/MissionSection.vue'

import FooterSection from './components/FooterSection.vue'

const appUrl = 'https://app.toolsedu.com'

function toApp() {
  try { fbq('track', 'LandingToApp') } catch (e) {} // eslint-disable-line
  window.location.href = appUrl
}
</script>

<template>
  <v-app>
    <LandingNav :app-url="appUrl" @go-app="toApp" />
    <v-main>
      <HeroSection @go-app="toApp" />
      <FeaturesSection />
      <HowItWorks />
      <TestimonialSection />
      <PricingSection @go-app="toApp" />
      <MissionSection />
      <FooterSection />
    </v-main>
  </v-app>
</template>

<style>
html {
  scroll-behavior: smooth;
}
body {
  background: #faf9f7;
}
</style>
