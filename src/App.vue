<script setup lang="ts">
import TheNav from './components/TheNav.vue'
import TheHero from './components/TheHero.vue'
import WhatWeDo from './components/WhatWeDo.vue'
import TrustBand from './components/TrustBand.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <div class="flex min-h-screen flex-col bg-paper text-ink">
    <TheNav />
    <main class="flex-1">
      <TheHero />
      <WhatWeDo />
      <TrustBand />
    </main>
    <TheFooter />
  </div>
</template>
