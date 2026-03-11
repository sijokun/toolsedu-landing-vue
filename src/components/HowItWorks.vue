<script setup>
const steps = [
  {
    num: '1',
    title: 'Describe Your Topic',
    desc: 'Enter any subject, vocabulary list, or learning objective. Choose the activity type and difficulty level.',
    icon: 'mdi-pencil-outline',
  },
  {
    num: '2',
    title: 'AI Generates It',
    desc: 'Our AI creates a complete, ready-to-use activity in seconds — crosswords, word searches, quizzes, and more.',
    icon: 'mdi-creation-outline',
  },
  {
    num: '3',
    title: 'Share & Play',
    desc: 'Share with students via a link. Track results, view leaderboards, and organize content into lessons and courses.',
    icon: 'mdi-share-variant-outline',
  },
]
</script>

<template>
  <section class="how-it-works py-16">
    <v-container style="max-width: 1200px;">
      <div class="text-center mb-12">
        <h2 class="section-title">How It Works</h2>
        <p class="section-subtitle">From idea to interactive activity in three simple steps.</p>
      </div>
      <v-row justify="center">
        <v-col v-for="(step, i) in steps" :key="step.num" cols="12" sm="4">
          <div class="text-center step-item">
            <div class="step-circle mx-auto mb-4">
              <v-icon color="white" size="28">{{ step.icon }}</v-icon>
            </div>
            <h3 class="step-title mb-2">{{ step.title }}</h3>
            <p class="step-desc">{{ step.desc }}</p>
          </div>
          <div v-if="i < steps.length - 1" class="step-connector d-none d-sm-block" />
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.section-title {
  font-size: 38px;
  font-weight: 700;
  color: #1e2248;
  margin-bottom: 12px;
}

.section-subtitle {
  font-size: 18px;
  color: #777;
}

.step-circle {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  background: linear-gradient(135deg, #785FEB 0%, #60a9f4 100%);
  display: flex;
  align-items: center;
  justify-content: center;
}

.step-title {
  font-size: 20px;
  font-weight: 600;
  color: #1e2248;
}

.step-desc {
  font-size: 15px;
  line-height: 1.5;
  color: #666;
  max-width: 300px;
  margin: 0 auto;
}

@media (max-width: 600px) {
  .section-title {
    font-size: 28px;
  }
}
</style>
