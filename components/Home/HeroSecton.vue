<template>
  <div class="hero">
    <div class="hero__content">
      <h1 class="hero__title">
        L'île de ré un des meilleurs destinations.
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero'

}
</script>

<style lang='scss' scoped>
  .hero {
    min-height: 985px;
    background-image: url(../../assets/images/hero.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center ;

    &__content {
      margin: 0 auto;
      max-width: 1192px;
      padding-top: 320px;
    }
    &__title {
      @include font(96px, 111px, white, bold)
    }
  }
</style>
