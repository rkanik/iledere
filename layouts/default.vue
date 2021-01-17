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

<style>
html {
  font-family: 'Banana Grotesk', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
