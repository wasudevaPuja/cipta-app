<script setup lang="ts">
const PROD_DOMAINS = [
  'ciptaniagasolution.com',
  'www.ciptaniagasolution.com'
]

const isProdDomain
  = typeof window !== 'undefined'
    && PROD_DOMAINS.includes(window.location.hostname)

useHead(() => {
  // jangan inject apa pun kalau bukan prod domain
  if (!import.meta.env.PROD || !isProdDomain) {
    return {
      link: [
        {
          rel: 'canonical',
          href: 'https://ciptaniagasolution.com'
        },
        {
          rel: 'icon',
          type: 'image/x-icon',
          sizes: '32x32',
          href: '/favicon-v2.ico'
        },
        {
          rel: 'icon',
          type: 'image/png',
          sizes: '32x32',
          href: '/favicon-v2.png'
        },
        {
          rel: 'icon',
          type: 'image/png',
          sizes: '16x16',
          href: '/favicon-v2.png'
        }
      ]
    }
  }

  // hanya jalan di ciptaniagasolution.com
  return {
    script: [
      {
        src: 'https://www.googletagmanager.com/gtag/js?id=G-VSBERFJM9Z',
        async: true
      },
      {
        innerHTML: `
          window.dataLayer = window.dataLayer || [];
          function gtag(){dataLayer.push(arguments);}
          gtag('js', new Date());
          gtag('config', 'G-VSBERFJM9Z');
        `,
        type: 'text/javascript'
      }
    ],
    link: [
      {
        rel: 'canonical',
        href: 'https://ciptaniagasolution.com'
      },
      {
        rel: 'icon',
        type: 'image/x-icon',
        sizes: '32x32',
        href: '/favicon-v2.ico'
      },
      {
        rel: 'icon',
        type: 'image/png',
        sizes: '32x32',
        href: '/favicon-v2.png'
      },
      {
        rel: 'icon',
        type: 'image/png',
        sizes: '16x16',
        href: '/favicon-v2.png'
      }
    ]
  }
})
</script>

<template>
  <div>
    <Navbar />

    <main>
      <NuxtPage />
      <FloatingButtons />
    </main>

    <Footer />
  </div>
</template>
