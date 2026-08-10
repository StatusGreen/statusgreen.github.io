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
      <div class="max-w-3xl">
        <img :src="sgLogo" alt="Status Green Solutions" class="mb-10 h-10 w-auto" />

        <h1 class="font-display text-[clamp(2.5rem,6vw,4.25rem)] font-extrabold leading-[1.05] tracking-[-0.01em] text-ink">
          Deep PowerChart Expertise.
          <span class="inline-block -rotate-1 rounded-sm bg-highlight px-2 py-0.5 text-ink">Direct Access.</span>
        </h1>

        <p class="mt-6 max-w-xl text-lg leading-relaxed text-ink/80">
          Status Green Solutions builds custom integrations and interoperability work embedded
          directly into Oracle Health Cerner PowerChart — delivered by a small team already
          trusted inside major hospital networks.
        </p>

        <div class="mt-8 flex flex-wrap items-center gap-4">
          <a
            href="mailto:info@statusgreensolutions.ca"
            class="rounded-full bg-primary px-6 py-3 font-display text-sm font-semibold text-neutral-white transition-colors hover:bg-[#003d2d]"
          >
            Contact Us
          </a>
          <a
            href="#what-we-do"
            class="rounded-full border border-ink/15 px-6 py-3 font-display text-sm font-semibold text-ink transition-colors hover:border-ink/30 hover:bg-ink/[0.03]"
          >
            See What We Do
          </a>
        </div>
      </div>

      <div class="mt-14 border-t border-grid-line pt-8">
        <p class="font-mono text-xs font-medium uppercase tracking-wide text-ink/50">
          Trusted inside hospital networks
        </p>
        <div class="mt-8 grid grid-cols-1 gap-10 sm:grid-cols-3 sm:gap-8">
          <div v-for="hospital in hospitals" :key="hospital.alt" class="flex flex-col items-center gap-3">
            <img
              :src="hospital.src"
              :alt="hospital.alt"
              class="h-37.5 w-auto object-contain grayscale transition-all duration-300 hover:grayscale-0"
            />
            <span class="text-sm font-medium text-ink/70">{{ hospital.alt }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
