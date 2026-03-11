<script setup>
defineProps(['appUrl'])
defineEmits(['goApp'])
</script>

<template>
  <v-app-bar flat color="rgba(255,255,255,0.9)" class="landing-nav" style="backdrop-filter: blur(12px);">
    <v-container class="d-flex align-center justify-space-between py-0" style="max-width: 1200px;">
      <div class="d-flex flex-column cursor-pointer" @click="$emit('goApp')">
        <img src="/images/header/logo.svg" alt="ToolsEdu" height="36" />
        <span class="by-cognenti">by Cognenti</span>
      </div>
      <div class="d-flex align-center ga-2">
        <v-btn
          variant="text"
          color="primary"
          href="#pricing"
          class="d-none d-sm-flex"
        >
          Pricing
        </v-btn>
        <v-btn
          variant="tonal"
          color="primary"
          rounded="lg"
          size="default"
          :href="appUrl"
        >
          Log in
        </v-btn>
        <v-btn
          color="primary"
          rounded="lg"
          size="default"
          :href="appUrl"
        >
          Get Started
          <v-icon end size="small">mdi-arrow-right</v-icon>
        </v-btn>
      </div>
    </v-container>
  </v-app-bar>
</template>

<style scoped>
.landing-nav {
  border-bottom: 1px solid rgba(0,0,0,0.06) !important;
}
.landing-nav .v-btn {
  height: 40px !important;
}
.by-cognenti {
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 0.5px;
  color: #785FEB;
  opacity: 0.6;
  margin-top: 0px;
  text-align: center;
}
</style>
