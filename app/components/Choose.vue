<template>
  <section
    id="why"
    class="relative py-16 lg:py-28 bg-[#0A1128] text-gray-200"
  >
    <div class="max-w-7xl mx-auto px-6">
      <!-- Section Header -->
      <div class="text-center mb-10 lg:mb-0">
        <p class="uppercase tracking-[0.3em] text-white/90 text-xs font-semibold mb-3">
          Why Clients Work With Us
        </p>
        <h2 class="text-3xl md:text-5xl font-bold text-white mb-3" data-aos="fade-up">
          Why Choose Us
        </h2>
        <p class="text-gray-400 text-sm md:text-base max-w-xl mx-auto" data-aos="fade-up">
          Partnering with PT Cipta Niaga Solutions means working with a team that prioritizes precision, trust, and long-term value.
        </p>
      </div>

      <div class="w-16 h-[2px] bg-[#2563EB] mx-auto rounded mt-6 mb-10 lg:mb-20" />

      <!-- Mobile: Compact stacked list -->
      <div class="flex flex-col divide-y divide-white/10 lg:hidden">
        <div
          v-for="(item, i) in whyUs"
          :key="item.title"
          class="flex items-start gap-4 py-5"
          data-aos="fade-up"
          :data-aos-delay="i * 40"
        >
          <!-- Icon badge -->
          <div class="w-10 h-10 rounded-xl bg-[#2563EB]/10 border border-[#2563EB]/20 flex items-center justify-center shrink-0">
            <UIcon :name="item.icon" class="w-5 h-5 text-[#2563EB]" />
          </div>
          <!-- Text -->
          <div>
            <h3 class="text-white font-semibold text-sm mb-1">{{ item.title }}</h3>
            <p class="text-gray-400 text-xs leading-relaxed font-light">{{ item.desc }}</p>
          </div>
        </div>
      </div>

      <!-- Desktop: Swiss border grid -->
      <div class="hidden lg:grid md:grid-cols-2 lg:grid-cols-3 border-t border-l border-white/10">
        <div
          v-for="(item, i) in whyUs"
          :key="item.title"
          class="p-10 md:p-12 border-b border-r border-white/10 relative group hover:bg-white/[0.02] transition-colors duration-500 flex flex-col"
          data-aos="fade-up"
          :data-aos-delay="i * 50"
        >
          <!-- Elegant background number -->
          <div class="absolute top-6 right-8 text-7xl font-serif font-bold text-white/5 group-hover:text-[#2563EB]/20 transition-colors duration-500 pointer-events-none select-none">
            0{{ i + 1 }}
          </div>

          <UIcon
            :name="item.icon"
            class="w-8 h-8 text-white mb-8 opacity-80 group-hover:scale-110 transition-transform duration-500 origin-left"
          />

          <h3 class="text-2xl text-white font-medium mb-4">
            {{ item.title }}
          </h3>

          <p class="text-gray-400 font-light leading-relaxed mt-auto">
            {{ item.desc }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const whyUs = [
  {
    title: 'Market Understanding',
    icon: 'mdi:chart-line',
    desc: 'Strong insight into trade dynamics and business environments.'
  },
  {
    title: 'Compliance & Reliability',
    icon: 'mdi:shield-check',
    desc: 'Operating in accordance with regulatory standards and business best practices.'
  },
  {
    title: 'Integrated Capabilities',
    icon: 'mdi:puzzle-outline',
    desc: 'Combining trading, advisory, and operational execution in one solution.'
  },
  {
    title: 'Professional Integrity',
    icon: 'mdi:handshake-outline',
    desc: 'Transparent and ethical approach in every engagement.'
  },
  {
    title: 'Extensive Network',
    icon: 'mdi:hub-outline',
    desc: 'Supported by trusted partners and reliable supplier connections.'
  },
  {
    title: 'Consistent Delivery',
    icon: 'mdi:check-all',
    desc: 'Focused on quality, efficiency, and dependable results.'
  }
]
</script>
