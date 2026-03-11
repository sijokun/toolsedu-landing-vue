<script setup>
</script>

<template>
  <footer class="footer py-8">
    <v-container style="max-width: 1200px;">
      <v-row align="center">
        <v-col cols="12" sm="4">
          <div class="d-flex align-center ga-2">
            <img src="/images/header/logo.svg" alt="ToolsEdu" height="28" />
          </div>
          <p class="text-caption text-grey mt-2">&copy; 2026 Cognenti LLC. All rights reserved.</p>
        </v-col>
        <v-col cols="12" sm="4" class="text-center">
          <p class="text-caption text-grey">
            30 N Gould St Ste N, Sheridan, WY 82801
          </p>
          <p class="text-caption text-grey">
            admins@toolsedu.com
          </p>
        </v-col>
        <v-col cols="12" sm="4" class="text-sm-end">
          <div class="d-flex ga-4 justify-sm-end">
            <a href="https://app.toolsedu.com/docs/privacy.txt" class="footer-link">Privacy Policy</a>
            <a href="https://app.toolsedu.com/docs/terms.txt" class="footer-link">Terms of Use</a>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </footer>
</template>

<style scoped>
.footer {
  border-top: 1px solid #eee;
}

.footer-link {
  font-size: 14px;
  color: #777;
  text-decoration: none;
  transition: color 0.2s;
}

.footer-link:hover {
  color: #785FEB;
}
</style>
