<template>
  <div class="error">
    <div class="container">
      <img class="error__image" src="../assets/svg/404.svg" alt="404 Image">
      <h4 class="error__title">
        Page Not Found
      </h4>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Error'

}
</script>

<style lang='scss' scoped>
  .error{
    padding: 70px 0;
    &__image {
      display: block;
      margin: 0 auto;
    }
    &__title {
      padding: 24px 0;
      margin-top: 24px;
      text-align: center;
      @include font(24px, 36px, #223263)
    }
  }
</style>
