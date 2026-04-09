<template>
  <section
    id="about"
    class="relative py-16 lg:py-28 bg-[#0A1128] text-gray-200"
  >
    <div class="absolute top-10 right-10 w-[460px] h-[460px] bg-white/10 rounded-full blur-3xl opacity-20" />

    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="grid lg:grid-cols-12 gap-10 lg:gap-24">
        
        <!-- Left Side: Huge Statement and Visual — Hidden on mobile -->
        <div class="hidden lg:flex lg:col-span-5 flex-col" data-aos="fade-right">
          <div class="flex items-center gap-4 mb-10">
            <div class="w-12 h-[1px] bg-[#2563EB]" />
            <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">
              Who We Are
            </p>
          </div>

          <h2 class="text-white text-5xl md:text-6xl font-light leading-[1.1] mb-12">
            Structuring <br>
            <span class="font-bold">Trade Flow</span><br>
            <span class="italic font-serif text-white">& Executive Strategy.</span>
          </h2>

          <!-- Elegant Abstract Graphic Container -->
          <div class="relative w-full aspect-[3/4] md:aspect-square lg:aspect-[3/4] rounded-tr-[4rem] rounded-bl-[4rem] overflow-hidden group">
            <div class="absolute inset-0 bg-[#0A1128] border border-white/5 bg-[radial-gradient(ellipse_at_top_right,rgba(255,255,255,0.15),transparent_60%)]" />
            <div class="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0MCIgaGVpZ2h0PSI0MCI+CjxyZWN0IHdpZHRoPSI0MCIgaGVpZ2h0PSI0MCIgZmlsbD0ibm9uZSIvPgo8Y2lyY2xlIGN4PSIyMCIgY3k9IjIwIiByPSIwLjUiIGZpbGw9InJnYmEoMjU1LDI1NSwyNTUsMC4wNSkiLz4KPC9zdmc+')] opacity-50" />
            
            <!-- Abstract Lines -->
            <div class="absolute bottom-10 left-10 right-10 flex flex-col gap-3 opacity-30 transform group-hover:-translate-y-4 transition-transform duration-700">
               <div class="h-[1px] w-full bg-gradient-to-r from-[#2563EB] to-transparent" />
               <div class="h-[1px] w-2/3 bg-gradient-to-r from-white to-transparent" />
               <div class="h-[1px] w-1/3 bg-gradient-to-r from-white to-transparent" />
            </div>
            
            <!-- Decorative Symbol -->
            <div class="absolute top-10 right-10 w-16 h-16 rounded-full border border-[#2563EB]/40 flex items-center justify-center animate-[spin_20s_linear_infinite]">
               <div class="w-2 h-2 rounded-full bg-[#2563EB]" />
            </div>
          </div>
        </div>

        <!-- Right Side: Content with Fine Typography -->
        <div class="lg:col-span-7 flex flex-col justify-center xl:pr-10" data-aos="fade-up">

          <!-- Mobile: Section label -->
          <div class="flex items-center gap-4 mb-6 lg:hidden">
            <div class="w-8 h-[1px] bg-[#2563EB]" />
            <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">Who We Are</p>
          </div>

          <!-- Lead quote -->
          <div class="pl-5 lg:pl-8 border-l-2 border-[#2563EB] mb-8 lg:mb-12">
            <p class="text-lg md:text-2xl lg:text-3xl text-white font-light leading-relaxed">
              PT Cipta Niaga Solutions was established to assist companies in navigating the complexities of modern trade and business operations with clarity, efficiency, and confidence.
            </p>
          </div>

          <!-- Body paragraphs -->
          <div class="space-y-5 lg:space-y-8 text-gray-400 text-base lg:text-lg leading-relaxed font-light">
            <p>
              Our approach is grounded in <span class="text-white font-medium">professionalism, accountability, and results-driven execution.</span> With experience in cross-border trade and business advisory, we help clients streamline operations, improve trade efficiency, and adapt to evolving market demands.
            </p>
            <p>
              Through a combination of structured processes, reliable networks, and practical business insight, we are committed to delivering consistent and measurable outcomes for our clients.
            </p>

            <!-- Closing badge -->
            <div class="pt-2 lg:pt-6">
              <div class="flex items-start gap-3 text-white text-sm font-medium border border-white/15 bg-white/5 px-5 py-4 rounded-2xl">
                <UIcon name="mdi:check-decagram-outline" class="w-5 h-5 text-[#2563EB] shrink-0 mt-0.5" />
                <span>At PT Cipta Niaga Solutions, we believe that strong execution and integrity are the foundation of long-term success.</span>
              </div>
            </div>
          </div>

          <!-- Highlight Divider -->
          <div class="h-[1px] w-full bg-gradient-to-r from-white/10 via-white/5 to-transparent mt-10 lg:mt-16" />
        </div>
      </div>
    </div>
  </section>
</template>
