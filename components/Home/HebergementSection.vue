<template>
  <div class="hebergement py-5">
    <div class="container">
      <SectionHeader class="hebergement__header" title="Top Hébergement" count="500+" />
      <vs-row class="hebergement__cards">
        <vs-col
          v-for="(res, index) in restaurants"
          :key="index"
          vs-w="3"
        >
          <ReserveCard v-bind="res" />
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>

<script>
import SectionHeader from '@/components/SectionHeader'
import ReserveCard from '@/components/Home/ReserveCard'
export default {
  name: 'HebergementSection',
  components: {
    SectionHeader,
    ReserveCard
  },
  data () {
    return {
      restaurants: [
        {
          thumbnail: require('../../assets/images/hebergement1.png'),
          name: 'Appartement Meublé',
          location: '13 rue Victor Henrri Saint Martin de Ré',
          bedroom: 5,
          bathroom: 3,
          cost: 10999
        },
        {
          thumbnail: require('../../assets/images/hebergement2.png'),
          name: 'La Veduta Di Vertine',
          location: '13 rue Victor Henrri Saint Martin de Ré',
          bedroom: 5,
          bathroom: 3,
          cost: 10999
        },
        {
          thumbnail: require('../../assets/images/hebergement3.png'),
          name: 'Appartement Meublé',
          location: '13 rue Victor Henrri Saint Martin de Ré',
          bedroom: 5,
          bathroom: 3,
          cost: 10999
        },
        {
          thumbnail: require('../../assets/images/hebergement4.png'),
          name: 'Appartement Meublé',
          location: '13 rue Victor Henrri Saint Martin de Ré',
          bedroom: 5,
          bathroom: 3,
          cost: 10999
        }
      ]
    }
  }
}
</script>

<style lang='scss' scoped>
  .hebergement {
    padding-top: 146px;
    &__header {
      margin-bottom: 58px;
    }
  }
</style>
