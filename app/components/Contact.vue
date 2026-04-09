<template>
  <section
    id="contact"
    class="relative py-16 lg:py-28 bg-[#0A1128] text-gray-200"
  >
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="border-t border-white/10 pt-10 lg:pt-20">

        <!-- Mobile compact header -->
        <div class="mb-8 lg:hidden" data-aos="fade-up">
          <div class="flex items-center gap-3 mb-3">
            <div class="w-8 h-[1px] bg-[#2563EB]" />
            <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">Get In Touch</p>
          </div>
          <h2 class="text-3xl font-light text-white leading-tight">
            Contact <span class="font-bold">Us.</span>
          </h2>
          <p class="text-gray-400 text-sm mt-2 font-light">
            We are ready to support your business with clarity, efficiency, and professionalism.
          </p>
        </div>

        <!-- Mobile: Compact contact info strip -->
        <div class="grid grid-cols-1 gap-3 mb-8 lg:hidden" data-aos="fade-up">
          <a href="mailto:ciptaniagasolution@gmail.com" class="flex items-center gap-3 bg-white/5 border border-white/10 rounded-xl px-4 py-3 hover:border-[#2563EB]/40 transition">
            <div class="w-8 h-8 rounded-lg bg-[#2563EB]/10 flex items-center justify-center shrink-0">
              <UIcon name="mdi:email-outline" class="w-4 h-4 text-[#2563EB]" />
            </div>
            <div>
              <p class="text-white/50 text-[10px] uppercase tracking-widest mb-0.5">Email</p>
              <p class="text-white text-xs font-medium break-all">ciptaniagasolution@gmail.com</p>
            </div>
          </a>
          <div class="flex items-center gap-3 bg-white/5 border border-white/10 rounded-xl px-4 py-3">
            <div class="w-8 h-8 rounded-lg bg-[#2563EB]/10 flex items-center justify-center shrink-0">
              <UIcon name="mdi:phone-outline" class="w-4 h-4 text-[#2563EB]" />
            </div>
            <div>
              <p class="text-white/50 text-[10px] uppercase tracking-widest mb-0.5">Phone</p>
              <p class="text-white text-xs font-medium">+62 882-100-77774</p>
            </div>
          </div>
          <div class="flex items-center gap-3 bg-white/5 border border-white/10 rounded-xl px-4 py-3">
            <div class="w-8 h-8 rounded-lg bg-[#2563EB]/10 flex items-center justify-center shrink-0">
              <UIcon name="mdi:map-marker-outline" class="w-4 h-4 text-[#2563EB]" />
            </div>
            <div>
              <p class="text-white/50 text-[10px] uppercase tracking-widest mb-0.5">Office</p>
              <p class="text-white text-xs font-medium leading-relaxed">Sahid Sudirman Center Lt. 23, Jakarta Pusat</p>
            </div>
          </div>
        </div>

        <div class="grid lg:grid-cols-2 gap-10 lg:gap-32">
          
          <!-- Text and Info (Left Col) — Desktop only -->
          <div class="hidden lg:flex flex-col justify-between" data-aos="fade-right">
            <div>
              <div class="flex items-center gap-4 mb-8">
                <div class="w-12 h-[1px] bg-[#2563EB]" />
                <p class="uppercase tracking-[0.3em] text-white text-xs font-bold">
                  Get In Touch
                </p>
              </div>
              
              <h2 class="text-5xl md:text-6xl font-light text-white mb-6 leading-[1.1]">
                Contact <br><span class="font-bold">Us.</span>
              </h2>
              
              <p class="text-gray-400 text-lg leading-relaxed font-light mb-16 max-w-md">
                We are ready to support your business with clarity, efficiency, and professionalism.
              </p>
            </div>

            <div class="space-y-10 border-l border-white/10 pl-8 relative">
               <div class="absolute -left-[1px] top-0 w-[1px] h-10 bg-white" />
               
               <div>
                 <p class="text-white text-[10px] uppercase tracking-[0.2em] mb-2 font-bold">Headquarters</p>
                 <p class="text-white font-light leading-relaxed">
                    Sahid Sudirman Center Lantai 23<br>
                    Jalan Jenderal Sudirman Kav. 86<br>
                    Karet Tengsin, Tanah Abang<br>
                    Jakarta Pusat 10220, Indonesia
                 </p>
               </div>
               
               <div>
                 <p class="text-white text-[10px] uppercase tracking-[0.2em] mb-2 font-bold">Inquiries</p>
                 <a href="mailto:ciptaniagasolution@gmail.com" class="text-white font-light hover:text-white pb-1 border-b border-white/20 hover:border-[#2563EB] transition break-all">
                    ciptaniagasolution@gmail.com
                 </a>
               </div>

               <div>
                 <p class="text-white text-[10px] uppercase tracking-[0.2em] mb-2 font-bold">Direct Line</p>
                 <p class="text-white font-light cursor-pointer hover:text-white transition">
                    +62 882-100-77774
                 </p>
               </div>
            </div>
          </div>

          <!-- Form (Right Col) -->
          <div data-aos="fade-up" data-aos-delay="100" class="lg:pt-10 flex flex-col justify-center">
            <form
              ref="contactForm"
              class="space-y-8 lg:space-y-12"
              @submit.prevent="submitForm"
            >
              <input type="hidden" name="access_key" value="eee4ad2d-7153-4a81-9610-0d69b1294b0c">

              <div class="grid md:grid-cols-2 gap-6 lg:gap-10">
                <div class="relative group">
                  <input
                    v-model="form.name" name="name" type="text" placeholder="Your Name" required
                    class="w-full pb-3 lg:pb-4 bg-transparent text-white border-b border-white/20 
                           placeholder-gray-600 focus:outline-none focus:border-[#2563EB] transition-colors rounded-none text-sm"
                  >
                  <div class="absolute bottom-0 left-0 w-0 h-[1px] bg-[#2563EB] group-focus-within:w-full transition-all duration-500" />
                </div>

                <div class="relative group">
                  <input
                    v-model="form.email" name="email" type="email" placeholder="Your Email" required
                    class="w-full pb-3 lg:pb-4 bg-transparent text-white border-b border-white/20 
                           placeholder-gray-600 focus:outline-none focus:border-[#2563EB] transition-colors rounded-none text-sm"
                  >
                  <div class="absolute bottom-0 left-0 w-0 h-[1px] bg-[#2563EB] group-focus-within:w-full transition-all duration-500" />
                </div>
              </div>

              <div class="relative group">
                <textarea
                  v-model="form.message" name="message" placeholder="How can we help you?" required
                  class="w-full h-28 lg:h-32 pb-4 bg-transparent text-white border-b border-white/20 
                         placeholder-gray-600 focus:outline-none focus:border-[#2563EB] transition-colors resize-none rounded-none text-sm"
                />
                <div class="absolute bottom-1.5 left-0 w-0 h-[1px] bg-[#2563EB] group-focus-within:w-full transition-all duration-500" />
              </div>

              <button
                type="submit"
                :disabled="loading"
                class="group relative w-full sm:w-auto inline-flex items-center justify-center gap-3 px-10 py-4 lg:py-5 bg-white text-[#0A1128] hover:bg-white font-bold tracking-widest uppercase text-xs transition-all duration-500 overflow-hidden cursor-pointer disabled:opacity-70 disabled:cursor-not-allowed"
              >
                <div class="absolute inset-0 w-0 bg-[#2563EB] transition-all duration-500 ease-out group-hover:w-full origin-left" />
                <span v-if="loading" class="animate-spin border-2 border-[#0A1128]/40 border-t-slate-950 rounded-full w-4 h-4 relative z-10" />
                <span class="relative z-10 transition-colors duration-300 group-hover:text-white">{{ loading ? 'Sending...' : 'Send Message' }}</span>
                <UIcon v-if="!loading" name="mdi:arrow-right" class="w-4 h-4 relative z-10 group-hover:translate-x-1 transition-transform duration-300" />
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import Swal from 'sweetalert2'

const loading = ref(false)
const contactForm = ref(null)

const form = ref({
  name: '',
  email: '',
  message: ''
})

const submitForm = async () => {
  loading.value = true

  const formData = new FormData(contactForm.value)

  try {
    const res = await fetch('https://api.web3forms.com/submit', {
      method: 'POST',
      body: formData
    }).then(r => r.json())

    loading.value = false

    if (res.success) {
      Swal.fire({
        title: 'Message Sent!',
        text: 'Thank you for contacting us. We\'ll get back to you shortly.',
        icon: 'success',
        confirmButtonColor: '#2563EB'
      })

      contactForm.value.reset()
      form.value = { name: '', email: '', message: '' }

      // Scroll back to Contact section
      document.getElementById('contact')?.scrollIntoView({
        behavior: 'smooth',
        block: 'start'
      })
    } else {
      throw new Error('Form submission failed')
    }
  } catch {
    loading.value = false

    Swal.fire({
      title: 'Error',
      text: 'Failed to send your message. Please try again.',
      icon: 'error',
      confirmButtonColor: '#EF4444'
    })
  }
}
</script>
