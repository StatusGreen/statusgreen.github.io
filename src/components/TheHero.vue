<script setup lang="ts">
import sgLogo from '../assets/sg-logo.svg'
import wrhnLogo from '../assets/hospitals/WRHN.png'
import niagaraHealthLogo from '../assets/hospitals/niagarahealth.png'
import wrhLogo from '../assets/hospitals/WRH.jpg'

const hospitals = [
  { src: wrhnLogo, alt: 'Waterloo Regional Health Network' },
  { src: niagaraHealthLogo, alt: 'Niagara Health' },
  { src: wrhLogo, alt: 'Windsor Regional Hospital' },
]
</script>

<template>
  <section id="top" class="relative overflow-hidden border-b border-grid-line">
    <div class="mx-auto max-w-6xl px-6 py-20 md:px-8 md:py-28">
      <div class="flex">
        <div class="max-w-3xl">
          <h1 class="font-display text-[clamp(2.5rem,6vw,4.25rem)] font-extrabold leading-[1.05] tracking-[-0.01em] text-ink">
            Technical Expertise,
            <span class="inline-block -rotate-1 rounded-sm bg-highlight px-2 py-0.5 text-ink">Custom to You.</span>
          </h1>
          <p class="mt-6 max-w-xl text-lg leading-relaxed text-ink/80">
            Status Green Solutions empowers clinicians with tools that are intuitive, compliant,
            and aligned with the realities of care delivery in Canada.
            Embedded directly into Oracle Health PowerChart — delivered by a skilled team, trusted by major Ontario hospital networks.
          </p>
        </div>
        <img :src="sgLogo" alt="Status Green Solutions" class="mb-10 w-auto" />
      </div>

      <div class="mt-14 border-t border-grid-line pt-8">
        <p class="text-xs font-medium uppercase tracking-wide text-ink/50">
          Trusted inside these hospital networks
        </p>
        <div class="mt-8 grid grid-cols-1 gap-10 sm:grid-cols-3 sm:gap-8">
          <div v-for="hospital in hospitals" :key="hospital.alt" class="flex flex-col items-center gap-3">
            <img
              :src="hospital.src"
              :alt="hospital.alt"
              class="h-37.5 w-auto object-contain grayscale transition-all duration-300 hover:grayscale-0"
            />
            <span class="text-sm font-medium text-ink/70 uppercase tracking-wide">{{ hospital.alt }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
