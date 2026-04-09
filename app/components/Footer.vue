<template>
  <footer class="relative bg-[#0A1128] text-gray-300 border-t border-white/10 overflow-hidden">
    <div class="absolute inset-0 pointer-events-none">
      <div class="absolute right-0 top-0 w-[380px] h-[380px] bg-white/10 rounded-full blur-3xl" />
      <div class="absolute left-0 bottom-0 w-[260px] h-[260px] bg-white/10 rounded-full blur-3xl" />
    </div>

    <div class="relative max-w-7xl mx-auto px-6 py-20 grid gap-14 sm:grid-cols-2 md:grid-cols-4">
      <div class="flex flex-col items-center text-center">
        <div
          class="w-30 h-30 rounded-3xl bg-white
           shadow-xl flex items-center justify-center mb-6"
        >
          <img
            src="/img/only_logo.png"
            alt="PT Cipta Niaga Solutions Logo"
            class="w-full h-full object-contain p-3"
          >
        </div>

        <p class="text-gray-400 text-sm leading-relaxed max-w-xs">
          Driving Smarter Business Across Borders
        </p>
      </div>

      <div>
        <h4 class="text-white font-semibold mb-5">
          Quick Links
        </h4>

        <ul class="space-y-3 text-sm">
          <li>
            <span
              class="cursor-pointer hover:text-white transition"
              @click="scrollTo('hero')"
            >Home</span>
          </li>
          <li>
            <span
              class="cursor-pointer hover:text-white transition"
              @click="scrollTo('about')"
            >About Us</span>
          </li>
          <li>
            <span
              class="cursor-pointer hover:text-white transition"
              @click="scrollTo('services')"
            >Services</span>
          </li>
          <li>
            <span
              class="cursor-pointer hover:text-white transition"
              @click="scrollTo('why')"
            >Why Work With Us</span>
          </li>
          <li>
            <span
              class="cursor-pointer hover:text-white transition"
              @click="scrollTo('partners')"
            >Our Partners</span>
          </li>
          <li>
            <span
              class="cursor-pointer hover:text-white transition"
              @click="scrollTo('contact')"
            >Contact</span>
          </li>
        </ul>
      </div>

      <div>
        <h4 class="text-white font-semibold mb-5">
          Company Info
        </h4>

        <p class="text-gray-400 text-sm leading-relaxed text-justify">
          <span class="text-white font-medium">PT CIPTA NIAGA SOLUTIONS</span><br>
          Sahid Sudirman Center Lantai 23<br>
          Jl. Jenderal Sudirman Kav. 86<br>
          Jakarta Pusat, Indonesia
        </p>

        <p class="mt-4 text-xs text-gray-500">
          Registered in Indonesia<br>
          NIB: 2402260139524<br>
          NPWP: 1000000008161052
        </p>
      </div>

      <div>
        <h4 class="text-white font-semibold mb-5">
          Contact
        </h4>

        <p class="text-sm mb-4">
          <span class="text-white font-medium">Email:</span><br>
          <a
            href="mailto:ciptaniagasolution@gmail.com"
            class="text-gray-300 hover:text-white underline underline-offset-2 transition break-all"
          >
            ciptaniagasolution@gmail.com
          </a>
        </p>

        <p class="text-sm mb-4">
          <span class="text-white font-medium">Phone:</span><br>
          +62 882-100-77774
        </p>
      </div>
    </div>

    <div class="relative text-center text-white text-sm border-t border-white/10 py-6">
      Copyright © 2026 PT Cipta Niaga Solutions. All rights reserved.
    </div>
  </footer>
</template>

<script setup>
const scrollTo = (id) => {
  const el = document.getElementById(id)
  if (el) el.scrollIntoView({ behavior: 'smooth' })
}
</script>
