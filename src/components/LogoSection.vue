<script setup>
const logos = [
  { src: '/logos/ocps.net.png', alt: 'Orange County Public Schools' },
  { src: '/logos/lasdschools.org.png', alt: 'LASD Schools' },
  { src: '/logos/ewingboe.org.png', alt: 'Ewing Board of Education' },
  { src: '/logos/calhounflschools.org.png', alt: 'Calhoun County Schools' },
  { src: '/logos/kells.ca.png', alt: 'Kells Academy' },
  { src: '/logos/edu.kristinehamn.se.svg', alt: 'Kristinehamn Education' },
  { src: '/logos/ztu.edu.ua.png', alt: 'ZTU Ukraine' },
  { src: '/logos/uaeh.edu.mx.png', alt: 'UAEH Mexico' },
  { src: '/logos/iies.edu.mx.png', alt: 'IIES Mexico' },
  { src: '/logos/cecar.edu.co.png', alt: 'CECAR Colombia' },
  { src: '/logos/lng.edu.co.png', alt: 'LNG Colombia' },
  { src: '/logos/becquerel.edu.ec.png', alt: 'Becquerel Ecuador' },
  { src: '/logos/perueduca.pe.svg', alt: 'PeruEduca' },
  { src: '/logos/www.firstasia.edu.ph.png', alt: 'First Asia Institute' },
]
</script>

<template>
  <section class="logos-section">
    <v-container style="max-width: 1200px;">
      <p class="text-center logos-heading mb-8">Trusted by educators from</p>
      <div class="logos-track-wrapper">
        <div class="logos-track">
          <img
            v-for="(logo, i) in [...logos, ...logos]"
            :key="i"
            :src="logo.src"
            :alt="logo.alt"
            class="logo-img"
          />
        </div>
      </div>
    </v-container>
  </section>
</template>

<style scoped>
.logos-section {
  padding: 40px 0 24px;
  overflow: hidden;
}

.logos-heading {
  font-size: 15px;
  font-weight: 500;
  color: #999;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.logos-track-wrapper {
  overflow: hidden;
  mask-image: linear-gradient(to right, transparent, black 10%, black 90%, transparent);
  -webkit-mask-image: linear-gradient(to right, transparent, black 10%, black 90%, transparent);
}

.logos-track {
  display: flex;
  align-items: center;
  gap: 48px;
  width: max-content;
  animation: scroll 60s linear infinite;
}

.logo-img {
  height: 40px;
  width: auto;
  object-fit: contain;
  filter: grayscale(100%);
  opacity: 0.5;
  transition: opacity 0.3s, filter 0.3s;
}

.logo-img:hover {
  filter: grayscale(0%);
  opacity: 1;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}
</style>
