<script setup lang="ts">
import sgLogo from './assets/sg-logo.svg'
import sgLogoGray from './assets/sg-logo-gray.svg'
</script>

<template>
  <header class="flex flex-col bg-[url(src/assets/terminal_banner.png)] bg-size-[750px] bg-top-right bg-no-repeat bg-black w-full">
    <div class="ml-auto mr-auto min-w-6xl">
      <img :src="sgLogoGray" alt="Status Green Solutions" />
    </div>
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