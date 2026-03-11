<script setup>
const audiences = [
  'Public Schools',
  'After-School Programs',
  'Individual Tutoring',
  'Preschools',
  'Community Classes',
  'Summer Camps',
  'Workshops',
]
</script>

<template>
  <section class="mission py-16">
    <v-container style="max-width: 900px;">
      <div class="text-center mb-8">
        <h2 class="section-title">Our Mission</h2>
        <p class="mission-text">
          ToolsEdu, a product of Cognenti LLC, is an EdTech platform helping teachers worldwide
          save time and create engaging lessons with AI.
        </p>
        <p class="mission-text mt-4">
          We believe every educator deserves access to powerful tools — from our free plan for
          individuals to team plans for schools and organizations.
        </p>
      </div>

      <div class="text-center mt-10">
        <p class="text-body-2 text-grey mb-4">No matter what type of program you run — we're on the same track</p>
        <div class="d-flex flex-wrap justify-center ga-2">
          <v-chip
            v-for="a in audiences"
            :key="a"
            variant="outlined"
            color="primary"
            rounded="lg"
            size="default"
          >
            {{ a }}
          </v-chip>
        </div>
      </div>
    </v-container>
  </section>
</template>

<style scoped>
.section-title {
  font-size: 38px;
  font-weight: 700;
  color: #1e2248;
  margin-bottom: 24px;
}

.mission-text {
  font-size: 18px;
  line-height: 1.6;
  color: #555;
}

@media (max-width: 600px) {
  .section-title {
    font-size: 28px;
  }
}
</style>
