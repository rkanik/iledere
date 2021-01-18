<template>
  <div class="partners">
    <div class="container">
      <vs-row vs-align="center" class="partners__row">
        <vs-col vs-w="2">
          <img src="../assets/images/partner1.png">
        </vs-col>
        <vs-col vs-w="2">
          <img src="../assets/images/partner2.png">
        </vs-col>
        <vs-col vs-w="2">
          <img src="../assets/images/partner5.png">
        </vs-col>
        <vs-col vs-w="2">
          <img src="../assets/images/partner3.png">
        </vs-col>
        <vs-col vs-w="2">
          <img src="../assets/images/partner4.png">
        </vs-col>
        <vs-col vs-w="2">
          <img src="../assets/images/partner5.png">
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Partners'
}
</script>

<style lang='scss' scoped>
  .partners {
    background-color: #223263;
    border-bottom: 2px solid rgba(#EBF0FF, 0.1);
    &__row {
      min-height: 196px;
    }
  }
</style>
