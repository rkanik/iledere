<template>
  <div id="app">
    <Header />
    <Nuxt />
  </div>
</template>

<script>
import Header from '@/components/Header'
export default {
  name: 'NoFooterLayout',
  components: {
    Header
  }
}
</script>
