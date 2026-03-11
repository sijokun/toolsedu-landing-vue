<script setup>
const stats = [
  { value: '19,000+', label: 'Teachers worldwide' },
  { value: '2,800+', label: 'Tasks generated daily' },
  { value: '4x', label: 'Faster lesson planning' },
]
</script>

<template>
  <section class="testimonials py-16">
    <v-container style="max-width: 1200px;">
      <v-row class="mb-12" justify="center">
        <v-col cols="12" sm="4" v-for="stat in stats" :key="stat.label">
          <div class="text-center">
            <div class="stat-value">{{ stat.value }}</div>
            <div class="stat-label">{{ stat.label }}</div>
          </div>
        </v-col>
      </v-row>

      <v-card rounded="xl" elevation="0" class="testimonial-card pa-8 mx-auto" style="max-width: 700px;">
        <div class="d-flex align-start ga-2 mb-4">
          <v-icon color="primary" size="20">mdi-format-quote-open</v-icon>
        </div>
        <p class="testimonial-text mb-6">
          If I take this platform away from my teachers, they'll throw me off the balcony.
        </p>
        <div class="d-flex align-center ga-3">
          <v-avatar color="primary" size="40">
            <span class="text-white text-body-2 font-weight-bold">LT</span>
          </v-avatar>
          <div>
            <div class="font-weight-bold" style="color: #1e2248;">Laura Tarr&eacute;s</div>
            <div class="text-caption text-grey">Cofounder of an online school</div>
          </div>
        </div>
      </v-card>
    </v-container>
  </section>
</template>

<style scoped>
.testimonials {
  background: #fff;
}

.stat-value {
  font-size: 42px;
  font-weight: 700;
  color: #785FEB;
  line-height: 1.2;
}

.stat-label {
  font-size: 16px;
  color: #777;
  margin-top: 4px;
}

.testimonial-card {
  border: 1px solid #f0eef5;
}

.testimonial-text {
  font-size: 22px;
  font-weight: 500;
  line-height: 1.4;
  color: #1e2248;
}

@media (max-width: 600px) {
  .stat-value {
    font-size: 32px;
  }
  .testimonial-text {
    font-size: 18px;
  }
}
</style>
