<script setup>
defineEmits(['goApp'])
</script>

<template>
  <section class="hero">
    <v-container style="max-width: 1200px;">
      <v-row align="center" class="py-16">
        <v-col cols="12" md="6">
          <div class="d-flex ga-2 mb-4">
            <v-chip color="primary" variant="tonal" size="small">AI-Powered</v-chip>
            <v-chip color="secondary" variant="tonal" size="small">Free to Start</v-chip>
          </div>
          <h1 class="hero-title mb-4">
            Create engaging lessons in seconds with AI.
          </h1>
          <p class="hero-subtitle mb-8">
            ToolsEdu helps educators create interactive worksheets, lessons, and courses.
            Crosswords, word searches, fill-in-the-blanks, matching, scrambles, and more — all generated in seconds.
          </p>
          <div class="d-flex ga-3 flex-wrap">
            <v-btn
              color="primary"
              size="large"
              rounded="lg"
              @click="$emit('goApp')"
            >
              Start Creating
              <v-icon end>mdi-arrow-right</v-icon>
            </v-btn>
            <v-btn
              variant="outlined"
              color="primary"
              size="large"
              rounded="lg"
              href="#pricing"
            >
              View Pricing
            </v-btn>
          </div>
          <p class="text-caption text-grey mt-3">No credit card required</p>
        </v-col>
        <v-col cols="12" md="6" class="d-flex justify-center">
          <img
            src="/images/header/admin.png"
            alt="ToolsEdu Dashboard"
            class="hero-image"
          />
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.hero {
  padding-top: 40px;
}

.hero-title {
  font-size: 48px;
  font-weight: 700;
  line-height: 1.15;
  color: #1e2248;
}

.hero-subtitle {
  font-size: 18px;
  line-height: 1.6;
  color: #555;
  max-width: 500px;
}

.hero-image {
  max-width: 100%;
  height: auto;
  border-radius: 16px;
}

@media (max-width: 960px) {
  .hero-title {
    font-size: 32px;
    text-align: center;
  }
  .hero-subtitle {
    text-align: center;
    max-width: 100%;
  }
  .hero .d-flex.ga-3 {
    justify-content: center;
  }
  .hero .text-caption {
    text-align: center;
  }
}
</style>
