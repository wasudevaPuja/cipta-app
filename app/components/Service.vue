<template>
  <section
    id="services"
    class="relative py-16 lg:py-28 bg-[#0A1128] text-gray-200"
  >
    <div class="max-w-7xl mx-auto px-6">

      <!-- Mobile: Compact header shown only on mobile -->
      <div class="lg:hidden mb-8" data-aos="fade-up">
        <div class="flex items-center gap-4 mb-4">
          <div class="w-8 h-[1px] bg-[#2563EB]" />
          <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">What We Do</p>
        </div>
        <h2 class="text-3xl font-light text-white leading-tight">
          Our <span class="font-bold">Services</span>
        </h2>
        <p class="text-gray-400 text-sm mt-2">Trade & Commercial Solutions</p>
      </div>

      <div class="grid lg:grid-cols-12 gap-0 lg:gap-24 items-start">
        
        <!-- Left Side: Sticky Title — Desktop only -->
        <div class="hidden lg:block lg:col-span-4 lg:sticky lg:top-32" data-aos="fade-right">
          <div class="flex items-center gap-4 mb-8">
            <div class="w-12 h-[1px] bg-[#2563EB]" />
            <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">
              What We Do
            </p>
          </div>
          
          <h2 class="text-4xl md:text-5xl lg:text-6xl font-light leading-[1.1] text-white mb-6">
            Our <br><span class="font-bold">Services</span>
          </h2>
          <p class="text-gray-400 text-lg font-light max-w-sm">
            Trade & Commercial Solutions
          </p>
        </div>

        <!-- Right Side: Clean Sequential List -->
        <div class="lg:col-span-8 flex flex-col" data-aos="fade-left">
          <div class="border-t border-white/10" />
          
          <div
            v-for="(service, i) in services"
            :key="service.title"
            class="py-8 md:py-16 border-b border-white/10 group"
          >
            <!-- Mobile: Icon + Number row -->
            <div class="flex items-center gap-3 mb-4 md:hidden">
              <div class="w-9 h-9 rounded-lg bg-white/5 border border-white/10 flex items-center justify-center">
                <UIcon :name="service.icon" class="w-4 h-4 text-[#2563EB]" />
              </div>
              <span class="text-white/40 font-serif text-sm border-l border-[#2563EB]/40 pl-3">0{{ i + 1 }}</span>
            </div>

            <div class="flex flex-col md:flex-row gap-4 md:gap-12">
              <!-- Number — Desktop only -->
              <div class="hidden md:flex shrink-0 items-start gap-4">
                <UIcon :name="service.icon" class="w-8 h-8 text-white/20 transition-colors group-hover:text-white" />
                <p class="text-white font-serif text-xl border-l border-[#2563EB]/50 pl-4">
                  0{{ i + 1 }}
                </p>
              </div>

              <!-- Content -->
              <div class="flex-grow">
                <h3 class="text-xl md:text-3xl font-medium text-white mb-3 md:mb-6">
                  {{ service.title }}
                </h3>
                
                <p class="text-gray-400 text-sm md:text-lg leading-relaxed font-light mb-5 md:mb-10">
                  {{ service.intro }}
                </p>
                
                <div class="grid sm:grid-cols-2 gap-x-8 gap-y-2 md:gap-y-4">
                  <div
                    v-for="(item, idx) in service.points"
                    :key="idx"
                    class="flex items-start gap-2 md:gap-3"
                  >
                    <div class="mt-2 w-1 h-1 rounded-full bg-[#2563EB] shrink-0 opacity-80" />
                    <span class="text-gray-300 text-sm md:text-[15px] font-light leading-relaxed">{{ item }}</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: 'Trade Execution & Sourcing',
    icon: 'mdi:swap-horizontal',
    intro:
      'We facilitate trading activities through structured import-export operations and tailored sourcing solutions across various product categories.',
    points: [
      'International trading (export & import)',
      'Customized sourcing based on client requirements',
      'Supplier identification and verification',
      'Flexible trading models (fee-based or contractual)'
    ]
  },
  {
    title: 'Business Support & Distribution',
    icon: 'mdi:truck-delivery-outline',
    intro:
      'We provide comprehensive support to ensure smooth transaction processes, regulatory compliance, and efficient delivery management.',
    points: [
      'Trade documentation and coordination',
      'Administrative and operational support',
      'Distribution planning aligned with business needs',
      'Domestic and international logistics coordination'
    ]
  },
  {
    title: 'Business & Management Consulting',
    icon: 'mdi:chart-timeline-variant',
    intro:
      'We support companies in enhancing their operational and strategic performance through structured advisory services.',
    points: [
      'Business process improvement',
      'Strategic planning and execution support',
      'Operational efficiency consulting',
      'Market and business advisory'
    ]
  }
]
</script>
