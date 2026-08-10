<script setup lang="ts">
const services = [
  {
    name: 'Custom PowerChart Integrations',
    dot: 'bg-primary ring-primary/30',
    description:
      'Custom functionality built directly into clinician-facing PowerChart workflows — embedded into the tools your team already uses, not bolted on as a separate system.',
  },
  {
    name: 'Data Interoperability & Interfacing',
    dot: 'bg-interop-blue ring-interop-blue/30',
    description:
      'Connecting PowerChart to the other systems your hospital network already runs, so data moves between them without manual re-entry.',
  },
]
</script>

<template>
  <section id="what-we-do" class="border-t border-grid-line bg-paper py-20 md:py-28">
    <div class="mx-auto max-w-6xl px-6 md:px-8">
      <h2 class="max-w-xl font-display text-3xl font-extrabold leading-tight text-ink md:text-4xl">
        What We Do
      </h2>

      <div class="mt-12 grid gap-12 md:grid-cols-2 md:gap-0 md:divide-x md:divide-grid-line">
        <div v-for="service in services" :key="service.name" class="md:pr-12 md:[&:nth-child(2)]:pl-12">
          <span class="inline-flex items-center gap-2">
            <span class="h-2.5 w-2.5 shrink-0 rounded-full ring-2" :class="service.dot" />
          </span>
          <h3 class="mt-3 font-display text-xl font-bold text-ink">{{ service.name }}</h3>
          <p class="mt-3 max-w-md text-base leading-relaxed text-ink/70">{{ service.description }}</p>
        </div>
      </div>

      <div class="mt-14 flex items-start gap-3 rounded-md border border-advisory-amber/25 bg-advisory-amber/[0.06] px-5 py-4">
        <span class="mt-1 h-2.5 w-2.5 shrink-0 rounded-full bg-advisory-amber ring-2 ring-advisory-amber/30" />
        <p class="text-sm leading-relaxed text-ink/70">
          Our full service catalog and case studies are being added here — check back soon,
          or <a href="mailto:info@statusgreensolutions.ca" class="font-semibold text-ink underline decoration-advisory-amber/50 underline-offset-2 hover:text-primary">get in touch</a>
          in the meantime.
        </p>
      </div>
    </div>
  </section>
</template>
