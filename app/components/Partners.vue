<template>
  <section
    id="partners"
    class="relative py-16 lg:py-28 bg-[#0A1128] text-gray-200 overflow-hidden"
  >
    <div class="max-w-7xl mx-auto px-6">
      <!-- Header -->
      <div class="flex flex-col items-center text-center mb-10 lg:mb-20">
        <div class="flex items-center justify-center gap-4 mb-4">
          <div class="w-8 lg:w-12 h-[1px] bg-[#2563EB]" />
          <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">
            Our Partners
          </p>
          <div class="w-8 lg:w-12 h-[1px] bg-[#2563EB]" />
        </div>

        <h2 class="text-3xl md:text-5xl font-light text-white mb-3" data-aos="fade-up">
          Collaborating for <span class="font-bold">Growth.</span>
        </h2>

        <p class="text-gray-400 text-sm md:text-lg font-light max-w-xl mx-auto" data-aos="fade-up" data-aos-delay="100">
          We work alongside trusted partners across industries to create sustainable value and long-term business success.
        </p>
      </div>
    </div>

    <!-- Marquee Row 1 — Left scroll -->
    <div class="overflow-hidden w-full flex group mask-horizontal relative mb-4 lg:mb-6">
      <div class="absolute inset-0 m-auto w-1/2 h-full bg-[#2563EB]/5 blur-[80px] pointer-events-none" />

      <div class="marquee-content shrink-0 flex items-center gap-10 md:gap-20 pr-10 md:pr-20">
        <div
          v-for="(partner, i) in partners"
          :key="'p1-' + partner.name"
          class="flex items-center justify-center w-24 md:w-40 h-14 md:h-20"
        >
          <img
            :src="partner.logo"
            :alt="partner.name"
            class="max-h-8 md:max-h-14 max-w-full object-contain grayscale opacity-30 hover:grayscale-0 hover:opacity-90 transition-all duration-500 cursor-pointer"
          >
        </div>
      </div>
      <div class="marquee-content shrink-0 flex items-center gap-10 md:gap-20 pr-10 md:pr-20" aria-hidden="true">
        <div
          v-for="(partner, i) in partners"
          :key="'p1b-' + partner.name"
          class="flex items-center justify-center w-24 md:w-40 h-14 md:h-20"
        >
          <img
            :src="partner.logo"
            :alt="partner.name"
            class="max-h-8 md:max-h-14 max-w-full object-contain grayscale opacity-30 hover:grayscale-0 hover:opacity-90 transition-all duration-500 cursor-pointer"
          >
        </div>
      </div>
    </div>

    <!-- Marquee Row 2 — Right scroll (mobile only adds visual depth) -->
    <div class="overflow-hidden w-full flex group mask-horizontal relative opacity-60">
      <div class="marquee-content-reverse shrink-0 flex items-center gap-10 md:gap-20 pr-10 md:pr-20">
        <div
          v-for="(partner, i) in [...partners].reverse()"
          :key="'p2-' + partner.name"
          class="flex items-center justify-center w-24 md:w-40 h-10 md:h-16"
        >
          <img
            :src="partner.logo"
            :alt="partner.name"
            class="max-h-6 md:max-h-10 max-w-full object-contain grayscale opacity-20 hover:grayscale-0 hover:opacity-70 transition-all duration-500 cursor-pointer"
          >
        </div>
      </div>
      <div class="marquee-content-reverse shrink-0 flex items-center gap-10 md:gap-20 pr-10 md:pr-20" aria-hidden="true">
        <div
          v-for="(partner, i) in [...partners].reverse()"
          :key="'p2b-' + partner.name"
          class="flex items-center justify-center w-24 md:w-40 h-10 md:h-16"
        >
          <img
            :src="partner.logo"
            :alt="partner.name"
            class="max-h-6 md:max-h-10 max-w-full object-contain grayscale opacity-20 hover:grayscale-0 hover:opacity-70 transition-all duration-500 cursor-pointer"
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const partners = [
  { name: 'Partner One', logo: '/img/ava.jpg' },
  { name: 'Partner Two', logo: '/img/ferron.png' },
  { name: 'Partner Three', logo: '/img/gufo.png' },
  { name: 'Partner Four', logo: '/img/nomaspect.png' },
  { name: 'Partner Five', logo: '/img/omega.jpg' },
  { name: 'Partner Six', logo: '/img/paradigm.png' },
  { name: 'Partner Seven', logo: '/img/qingdao.jpeg' },
  { name: 'Partner Eight', logo: '/img/shannon.png' },
  { name: 'Partner Nine', logo: '/img/sprawdzaj.svg' }
]
</script>

<style scoped>
.marquee-content {
  animation: scroll-left 35s linear infinite;
}

.marquee-content-reverse {
  animation: scroll-right 45s linear infinite;
}

/* Pause on hover */
.group:hover .marquee-content,
.group:hover .marquee-content-reverse {
  animation-play-state: paused;
}

/* Fade edges */
.mask-horizontal {
  mask-image: linear-gradient(to right, transparent, black 8%, black 92%, transparent);
  -webkit-mask-image: linear-gradient(to right, transparent, black 8%, black 92%, transparent);
}

@keyframes scroll-left {
  0% { transform: translateX(0); }
  100% { transform: translateX(-100%); }
}

@keyframes scroll-right {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(0); }
}
</style>
