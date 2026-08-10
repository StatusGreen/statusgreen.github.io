<script setup lang="ts">
import { ref } from 'vue'

const mobileOpen = ref(false)

const links = [
  { label: 'What We Do', href: '#what-we-do' },
  { label: 'Trust', href: '#trust' },
  { label: 'Contact', href: '#contact' },
]
</script>

<template>
  <header class="sticky top-0 z-40 border-b border-grid-line bg-paper/90 backdrop-blur-sm">
    <div class="mx-auto flex max-w-6xl items-center justify-between px-6 py-4 md:px-8">
      <nav class="hidden items-center gap-8 md:flex">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="group flex items-center gap-2 font-display text-sm font-semibold text-ink transition-colors hover:text-primary"
        >
          <span class="h-2 w-2 rounded-full bg-primary ring-2 ring-primary/30 transition-transform group-hover:scale-125" />
          {{ link.label }}
        </a>
      </nav>

      <div class="hidden items-center gap-4 md:flex">
        <a
          href="mailto:info@statusgreensolutions.ca"
          class="rounded-full bg-primary px-5 py-2 font-display text-sm font-semibold text-neutral-white transition-colors hover:bg-[#003d2d]"
        >
          Contact Us
        </a>
      </div>

      <button
        type="button"
        class="flex h-10 w-10 items-center justify-center rounded-md md:hidden"
        :aria-expanded="mobileOpen"
        aria-controls="mobile-nav"
        aria-label="Toggle navigation menu"
        @click="mobileOpen = !mobileOpen"
      >
        <svg v-if="!mobileOpen" class="h-6 w-6 text-ink" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else class="h-6 w-6 text-ink" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <div v-if="mobileOpen" id="mobile-nav" class="border-t border-grid-line px-6 py-4 md:hidden">
      <nav class="flex flex-col gap-4">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="flex items-center gap-2 font-display text-base font-semibold text-ink"
          @click="mobileOpen = false"
        >
          <span class="h-2 w-2 rounded-full bg-primary ring-2 ring-primary/30" />
          {{ link.label }}
        </a>
        <a
          href="mailto:info@statusgreensolutions.ca"
          class="mt-2 rounded-full bg-primary px-5 py-2.5 text-center font-display text-sm font-semibold text-neutral-white"
        >
          Contact Us
        </a>
      </nav>
    </div>
  </header>
</template>
