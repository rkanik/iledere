<template>
  <div id="app">
    <Header />
    <Nuxt />
    <Partners />
    <Footer />
  </div>
</template>

<script>

import Header from '@/components/Header'
import Partners from '@/components/Partners'
import Footer from '@/components/Footer'

export default {
  name: 'DefaultLayout',
  components: {
    Header,
    Partners,
    Footer
  }
}
</script>
