<template>
  <div
    class="fixed bottom-6 right-6 flex flex-col gap-4 z-[9999] pointer-events-auto"
  >
    <button
      class="w-14 h-14 rounded-full bg-[#2563EB] hover:bg-[#1D4ED8] text-white font-bold flex items-center justify-center shadow-[0_8px_30px_-4px_rgba(255,255,255,0.4)] transition-all active:scale-95 cursor-pointer"
      aria-label="Scroll to Top"
      @click="scrollToTop"
    >
      <span class="text-2xl">↑</span>
    </button>
  </div>
</template>

<script setup>
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}
</script>
