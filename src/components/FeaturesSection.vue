<script setup>
const features = [
  {
    icon: 'mdi-puzzle-outline',
    title: 'Crosswords',
    desc: 'AI generates themed crossword puzzles from any topic or vocabulary list.',
    color: '#785FEB',
  },
  {
    icon: 'mdi-magnify',
    title: 'Word Searches',
    desc: 'Create word search grids with hidden words tailored to your lesson.',
    color: '#60a9f4',
  },
  {
    icon: 'mdi-text-box-outline',
    title: 'Fill the Gaps',
    desc: 'Generate cloze exercises that test comprehension and vocabulary.',
    color: '#f59e42',
  },
  {
    icon: 'mdi-vector-link',
    title: 'Matching',
    desc: 'Pair terms with definitions, translations, or images automatically.',
    color: '#43b87a',
  },
  {
    icon: 'mdi-checkbox-marked-circle-outline',
    title: 'Multiple Choice',
    desc: 'Create quizzes with AI-generated questions and answer options.',
    color: '#e0534a',
  },
  {
    icon: 'mdi-shuffle-variant',
    title: 'Scrambles',
    desc: 'Unscramble words and sentences for engaging language practice.',
    color: '#7a71c8',
  },
]
</script>

<template>
  <section class="features py-16">
    <v-container style="max-width: 1200px;">
      <div class="text-center mb-12">
        <h2 class="section-title">Six Activity Types, One Platform</h2>
        <p class="section-subtitle">Design interactive activities in seconds, tailored to any topic or grade level.</p>
      </div>
      <v-row>
        <v-col v-for="f in features" :key="f.title" cols="12" sm="6" md="4">
          <v-card
            rounded="xl"
            elevation="0"
            class="feature-card pa-6 h-100"
          >
            <v-icon :color="f.color" size="36" class="mb-4">{{ f.icon }}</v-icon>
            <h3 class="feature-title mb-2">{{ f.title }}</h3>
            <p class="feature-desc">{{ f.desc }}</p>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.features {
  background: #fff;
}

.section-title {
  font-size: 38px;
  font-weight: 700;
  color: #1e2248;
  margin-bottom: 12px;
}

.section-subtitle {
  font-size: 18px;
  color: #777;
  max-width: 550px;
  margin: 0 auto;
}

.feature-card {
  border: 1px solid #f0eef5;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 30px rgba(120, 95, 235, 0.08);
}

.feature-title {
  font-size: 20px;
  font-weight: 600;
  color: #1e2248;
}

.feature-desc {
  font-size: 15px;
  line-height: 1.5;
  color: #666;
}

@media (max-width: 600px) {
  .section-title {
    font-size: 28px;
  }
}
</style>
