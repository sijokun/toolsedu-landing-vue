<script setup>
import { ref, computed } from 'vue'

defineEmits(['goApp'])

const yearly = ref(false)

const plans = [
  {
    name: 'Free',
    monthlyPrice: 0,
    yearlyPrice: 0,
    features: ['Limited Worksheet Generation', '3 per day / 10 per week'],
    cta: 'Get Started',
  },
  {
    name: 'Basic',
    monthlyPrice: 3,
    yearlyPrice: 30,
    features: ['More Worksheet Generation', 'Lessons'],
    cta: 'Get Started',
  },
  {
    name: 'Pro',
    monthlyPrice: 5,
    yearlyPrice: 50,
    popular: true,
    features: ['More Worksheet Generation', 'Lessons', 'Courses', 'Play'],
    cta: 'Get Started',
  },
  {
    name: 'Unlimited',
    monthlyPrice: 10,
    yearlyPrice: 100,
    features: ['Unlimited Worksheet Generation', 'Lessons', 'Courses', 'Play', 'Priority Support'],
    cta: 'Get Started',
  },
]

function formatPrice(plan) {
  const price = yearly.value ? plan.yearlyPrice : plan.monthlyPrice
  if (price === 0) return '$0'
  return `$${price % 1 === 0 ? price : price.toFixed(2)}`
}

function periodLabel(plan) {
  if (plan.monthlyPrice === 0) return 'forever'
  return yearly.value ? '/year' : '/month'
}
</script>

<template>
  <section class="pricing py-16" id="pricing">
    <v-container style="max-width: 1200px;">
      <div class="text-center mb-4">
        <h2 class="section-title">Simple, Transparent Pricing</h2>
        <p class="section-subtitle">Start free. Upgrade when you need more.</p>
      </div>

      <div class="d-flex align-center justify-center ga-3 mb-10">
        <span :class="['toggle-label', { active: !yearly }]">Monthly</span>
        <v-switch
          v-model="yearly"
          hide-details
          density="compact"
          color="primary"
          inset
          class="flex-grow-0"
        />
        <span :class="['toggle-label', { active: yearly }]">
          Yearly
          <v-chip size="x-small" color="primary" variant="tonal" class="ml-1">Save up to 17%</v-chip>
        </span>
      </div>

      <v-row justify="center">
        <v-col v-for="plan in plans" :key="plan.name" cols="12" sm="6" md="3">
          <v-card
            rounded="xl"
            elevation="0"
            :class="['pricing-card pa-6 h-100 d-flex flex-column', { 'pricing-card--popular': plan.popular }]"
          >
            <v-chip
              v-if="plan.popular"
              color="primary"
              size="small"
              class="popular-badge"
            >
              Most Popular
            </v-chip>

            <div class="mb-6">
              <div class="plan-name mb-2">{{ plan.name }}</div>
              <div class="d-flex align-baseline ga-1">
                <span class="plan-price">{{ formatPrice(plan) }}</span>
                <span class="plan-period">{{ periodLabel(plan) }}</span>
              </div>
            </div>

            <v-divider class="mb-4" />

            <div class="flex-grow-1 mb-6">
              <div
                v-for="feature in plan.features"
                :key="feature"
                class="d-flex align-center ga-2 mb-3"
              >
                <v-icon color="primary" size="18">mdi-check-circle</v-icon>
                <span class="feature-text">{{ feature }}</span>
              </div>
            </div>

            <v-btn
              :color="plan.popular ? 'primary' : undefined"
              :variant="plan.popular ? 'flat' : 'tonal'"
              block
              rounded="lg"
              @click="$emit('goApp')"
            >
              {{ plan.cta }}
            </v-btn>
          </v-card>
        </v-col>
      </v-row>

      <p class="text-center text-caption text-grey mt-6">
        Cancel anytime. No long-term contracts. Cancellation takes effect at the end of your billing period.
      </p>
    </v-container>
  </section>
</template>

<style scoped>
.pricing {
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
}

.toggle-label {
  font-size: 15px;
  font-weight: 500;
  color: #999;
  transition: color 0.2s;
}

.toggle-label.active {
  color: #1e2248;
}

.pricing-card {
  border: 1px solid #f0eef5;
  position: relative;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.pricing-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 30px rgba(120, 95, 235, 0.08);
}

.pricing-card--popular {
  border: 2px solid #785FEB;
}

.popular-badge {
  position: absolute;
  top: -12px;
  left: 50%;
  transform: translateX(-50%);
}

.plan-name {
  font-size: 18px;
  font-weight: 600;
  color: #1e2248;
}

.plan-price {
  font-size: 36px;
  font-weight: 700;
  color: #1e2248;
  line-height: 1;
}

.plan-period {
  font-size: 14px;
  color: #999;
}

.feature-text {
  font-size: 14px;
  color: #555;
}

.pricing-card .v-btn {
  height: 44px !important;
}

@media (max-width: 600px) {
  .section-title {
    font-size: 28px;
  }
}
</style>
