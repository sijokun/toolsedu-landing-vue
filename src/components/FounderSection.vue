<script setup>
</script>

<template>
  <section class="founder py-16">
    <v-container style="max-width: 900px;">
      <h2 class="section-title text-center mb-10">About the Founder</h2>
      <v-card rounded="xl" elevation="0" class="founder-card pa-8">
        <div class="d-flex align-center ga-8 flex-wrap justify-center">
          <v-avatar size="140" class="founder-avatar flex-shrink-0">
            <v-img src="/images/kseniia.jpg" alt="Kseniia Lukina" cover />
          </v-avatar>
          <div class="founder-info">
            <h3 class="founder-name mb-1">Kseniia Lukina</h3>
            <p class="founder-role mb-3">EdTech developer and CEO of Cognenti LLC</p>
            <p class="founder-desc">
              Founder of ToolsEdu, an AI-powered platform helping teachers worldwide create
              personalized lessons in seconds. ToolsEdu already supports over 19,000 educators globally.
            </p>
          </div>
        </div>
      </v-card>
    </v-container>
  </section>
</template>

<style scoped>
.founder {
  background: #fff;
}

.section-title {
  font-size: 38px;
  font-weight: 700;
  color: #1e2248;
}

.founder-card {
  border: 1px solid #f0eef5;
}

.founder-avatar {
  border: 3px solid #785FEB;
}

.founder-info {
  max-width: 500px;
}

.founder-name {
  font-size: 24px;
  font-weight: 700;
  color: #1e2248;
}

.founder-role {
  font-size: 16px;
  font-weight: 500;
  color: #785FEB;
}

.founder-desc {
  font-size: 15px;
  line-height: 1.6;
  color: #555;
}

@media (max-width: 600px) {
  .section-title {
    font-size: 28px;
  }
  .founder-info {
    text-align: center;
  }
}
</style>
