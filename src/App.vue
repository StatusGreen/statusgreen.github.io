<script setup lang="ts">
import sgLogo from './assets/sg-logo.svg'
import sgLogoGray from './assets/sg-logo-gray.svg'
</script>

<template>
  <header class="flex flex-col justify-center items-center bg-linear-to-b from-gray-400 to-gray-100">
    <img :src="sgLogo" alt="Status Green Solutions" />
  </header>
  <footer class="flex flex-col bg-gray-800 text-gray-100">
    <div class="ml-auto mr-auto min-w-6xl">
      <div class="flex justify-between items-center">
        <img :src="sgLogoGray" alt="Status Green Solutions" width="200px">
        <div class="flex flex-col">
          <span class="text-2xl font-bold">Contact Info</span>
          <span>info@statusgreensolutions.ca</span>
        </div>
      </div>
      <div class="border-t border-t-gray-400 pt-2 pb-2">&copy; Status Green Soltuions. All Rights Reserved</div>
    </div>
  </footer>
</template>