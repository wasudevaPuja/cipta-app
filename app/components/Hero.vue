<template>
  <section id="hero"
    class="relative min-h-screen flex items-center justify-center overflow-hidden bg-[#0A1128] pt-20 pb-16 md:pt-0 md:pb-0">
    <div class="absolute inset-0
         bg-[#0A1128]" />

    <div class="absolute top-[35%] left-1/2 -translate-x-1/2
         w-[900px] h-[900px]
         bg-[radial-gradient(circle,rgba(255,255,255,0.3),rgba(255,255,255,0.05),transparent)]
         blur-[90px] opacity-70 pointer-events-none" />

    <div class="absolute bottom-[-120px] left-1/2 -translate-x-1/2
         w-[1400px] h-[600px]
         bg-[radial-gradient(circle_at_bottom,rgba(255,255,255,0.35),transparent_70%)]
         blur-[160px] opacity-80" />

    <div class="absolute inset-0
         bg-[radial-gradient(circle,transparent_55%,rgba(0,0,0,0.55)_100%)]" />

    <div class="absolute inset-0 opacity-[0.07] pointer-events-none"
      style="background-image:url('data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'300\' height=\'300\'><filter id=\'n\'><feTurbulence type=\'fractalNoise\' baseFrequency=\'0.8\' numOctaves=\'5\'/></filter><rect width=\'100%\' height=\'100%\' filter=\'url(%23n)\'/></svg>');" />

    <div class="relative z-10 w-full max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-16 items-center">
      <!-- Left Content -->
      <div data-aos="fade-right">
        <!-- Company pill badge -->
        <div
          class="inline-flex items-center gap-2 px-3 py-1.5 lg:px-4 lg:py-2 rounded-full bg-white/10 border border-white/20 mb-5 lg:mb-8">
          <span class="w-1.5 h-1.5 lg:w-2 lg:h-2 rounded-full bg-[#2563EB] animate-pulse" />
          <p class="uppercase tracking-[0.15em] lg:tracking-[0.2em] text-white text-[10px] lg:text-xs font-bold">
            PT CIPTA NIAGA SOLUTIONS
          </p>
        </div>

        <!-- Main heading — tighter on mobile -->
        <h1
          class="text-white font-extrabold leading-[1.1] text-4xl sm:text-5xl lg:text-[4.5rem] drop-shadow-sm mb-4 lg:mb-6">
          Trade.<br>
          Insight.<br>
          <span class="text-white italic font-serif relative">
            Execution.
            <svg class="absolute -bottom-2 left-0 w-full h-3 text-[#2563EB]/80" viewBox="0 0 100 10"
              preserveAspectRatio="none">
              <path d="M0 5 Q 50 10 100 5" stroke="currentColor" stroke-width="2" fill="none" />
            </svg>
          </span>
        </h1>

        <!-- Mobile: short tagline only -->
        <p class="text-white font-medium text-sm mb-6 lg:hidden">
          Driving Smarter Business Across Borders
        </p>

        <!-- Desktop: full paragraph -->
        <p class="hidden lg:block text-gray-300 text-lg md:text-xl leading-relaxed max-w-lg mb-10" data-aos="fade-up"
          data-aos-delay="150">
          <span class="text-white font-medium block mb-2">Driving Smarter Business Across Borders</span>
          We empower businesses to operate more effectively in today's dynamic trade environment—by connecting
          opportunities, refining strategies, and delivering structured execution for sustainable growth.
        </p>

        <!-- Buttons -->
        <div class="flex flex-col sm:flex-row flex-wrap items-stretch sm:items-center gap-3 sm:gap-5 w-full"
          data-aos="fade-up" data-aos-delay="300">
          <button
            class="w-full sm:w-auto px-6 lg:px-8 py-3.5 lg:py-4 bg-[#2563EB] hover:bg-[#1D4ED8] text-white rounded-xl
                   font-bold shadow-[0_8px_30px_-4px_rgba(37,99,235,0.5)]
                   transition-all duration-300 active:scale-[0.98] cursor-pointer inline-flex justify-center items-center gap-2 text-sm"
            @click="scrollTo('about')">
            Discover More
            <UIcon name="mdi:arrow-right" class="w-4 h-4" />
          </button>

          <button class="w-full sm:w-auto px-6 lg:px-8 py-3.5 lg:py-4 bg-white/5 border border-white/20 text-white rounded-xl font-medium text-sm
                   hover:bg-white/10 hover:border-[#2563EB] transition-all duration-200 cursor-pointer text-center"
            @click="scrollTo('contact')">
            Get In Touch
          </button>
        </div>
      </div>

      <!-- Right Visual (Abstract Interface / Cards) -->
      <div class="hidden lg:block relative h-[600px] w-full perspective-1000" data-aos="fade-left" data-aos-delay="200">
        <!-- Card 1 — Trade Execution -->
        <div
          class="absolute top-10 right-10 w-[350px] h-[400px] bg-[#0A1128]/60 backdrop-blur-2xl border border-white/10 rounded-3xl p-6 shadow-2xl transform rotate-3 hover:rotate-0 transition-transform duration-700 z-20">
          <div class="flex items-center justify-between border-b border-white/10 pb-4 mb-4">
            <div class="text-[#2563EB] text-xs font-bold tracking-widest uppercase">Trade Execution</div>
            <UIcon name="mdi:swap-horizontal" class="text-white w-6 h-6" />
          </div>
          <div class="space-y-3 mb-6">
            <div class="flex items-center gap-3">
              <div class="w-1.5 h-1.5 rounded-full bg-[#2563EB] shrink-0" />
              <div class="h-2 w-3/4 bg-white/10 rounded-full" />
            </div>
            <div class="flex items-center gap-3">
              <div class="w-1.5 h-1.5 rounded-full bg-white/30 shrink-0" />
              <div class="h-2 w-1/2 bg-white/10 rounded-full" />
            </div>
            <div class="flex items-center gap-3">
              <div class="w-1.5 h-1.5 rounded-full bg-[#2563EB]/60 shrink-0" />
              <div class="h-2 w-5/6 bg-white/20 rounded-full" />
            </div>
            <div class="flex items-center gap-3">
              <div class="w-1.5 h-1.5 rounded-full bg-white/30 shrink-0" />
              <div class="h-2 w-2/3 bg-white/10 rounded-full" />
            </div>
          </div>
        </div>

        <!-- Card 2 — Business Advisory -->
        <div
          class="absolute bottom-20 left-10 w-[280px] h-auto bg-white/5 backdrop-blur-md border border-[#2563EB]/20 rounded-3xl p-6 shadow-2xl transform -rotate-6 hover:rotate-0 transition-transform duration-700 z-30">
          <div class="w-12 h-12 rounded-xl bg-[#2563EB]/15 border border-[#2563EB]/25 flex items-center justify-center mb-5">
            <UIcon name="mdi:briefcase-outline" class="text-[#2563EB] w-6 h-6" />
          </div>
          <div class="text-lg font-semibold text-white mb-1">Business Advisory</div>
          <div class="text-xs text-gray-400 leading-relaxed mb-5">Structured consulting for operational and strategic performance.</div>
          <!-- Capability badges -->
          <div class="space-y-2">
            <div class="flex items-center gap-3 bg-white/5 border border-white/10 rounded-xl px-3 py-2.5">
              <div class="w-6 h-6 rounded-lg bg-[#2563EB]/20 flex items-center justify-center shrink-0">
                <UIcon name="mdi:check" class="w-3.5 h-3.5 text-[#2563EB]" />
              </div>
              <span class="text-xs text-white font-medium">Strategic Planning & Execution</span>
            </div>
            <div class="flex items-center gap-3 bg-white/5 border border-white/10 rounded-xl px-3 py-2.5">
              <div class="w-6 h-6 rounded-lg bg-[#2563EB]/20 flex items-center justify-center shrink-0">
                <UIcon name="mdi:check" class="w-3.5 h-3.5 text-[#2563EB]" />
              </div>
              <span class="text-xs text-white font-medium">Operational Efficiency Consulting</span>
            </div>
            <div class="flex items-center gap-3 bg-white/5 border border-white/10 rounded-xl px-3 py-2.5">
              <div class="w-6 h-6 rounded-lg bg-[#2563EB]/20 flex items-center justify-center shrink-0">
                <UIcon name="mdi:check" class="w-3.5 h-3.5 text-[#2563EB]" />
              </div>
              <span class="text-xs text-white font-medium">Market & Business Advisory</span>
            </div>
          </div>
        </div>

        <!-- Abstract Glows behind cards -->
        <div
          class="absolute inset-0 bg-gradient-to-tr from-transparent via-[#2563EB]/10 to-transparent rounded-full blur-3xl opacity-50 z-10" />
      </div>
    </div>
  </section>
</template>

<script setup>
const scrollTo = (id) => {
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
}
</script>
