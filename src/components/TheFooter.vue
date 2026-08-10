<script setup lang="ts">
import sgLogoGray from '../assets/sg-logo-gray.svg'

const year = new Date().getFullYear()
</script>

<template>
  <footer id="contact" class="border-t border-neutral-white/10 bg-surface-dark text-neutral-white">
    <div class="mx-auto max-w-6xl px-6 py-14 md:px-8">
      <div class="flex flex-col items-start justify-between gap-8 md:flex-row md:items-center">
        <img :src="sgLogoGray" alt="Status Green Solutions" class="h-10 w-auto" />

        <div class="flex flex-col gap-1">
          <span class="font-display text-lg font-bold">Contact Info</span>
          <a
            href="mailto:info@statusgreensolutions.ca"
            class="font-mono text-sm text-neutral-white/70 transition-colors hover:text-highlight"
          >
            info@statusgreensolutions.ca
          </a>
        </div>
      </div>

      <div class="mt-10 flex flex-col gap-2 border-t border-divider-gray/30 pt-6 text-xs text-neutral-white/50 md:flex-row md:items-center md:justify-between">
        <span>&copy; {{ year }} Status Green Solutions. All rights reserved.</span>
        <span>Canada</span>
      </div>
    </div>
  </footer>
</template>
