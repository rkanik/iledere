<template>
  <div class="restaurant py-5">
    <div class="container">
      <SectionHeader class="restaurant__header" title="Top Restaurants" count="200+" />
      <vs-row
        vs-justify="center"
        vs-align="center"
        class="restaurant__cards"
      >
        <vs-col
          v-for="(res, index) in restaurants"
          :key="index"
          vs-w="3"
          vs-xs='12'
        >
          <ReserveCard v-bind="res" type="restaurant" />
        </vs-col>
      </vs-row>
      <div class="sechead__more von-mobile">
				Voir plus
				<i class="bx bx-arrow-back" />
			</div>
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
          thumbnail: require('../../assets/images/restaurant1.png'),
          name: 'Restautant Le Bordin Zinc',
          location: '13 rue Victor Henrri Saint Martin de Ré'
        },
        {
          thumbnail: require('../../assets/images/restaurant2.png'),
          name: 'Restautant Bistrot-Couteaux',
          location: '13 rue Victor Henrri Saint Martin de Ré'
        },
        {
          thumbnail: require('../../assets/images/restaurant3.png'),
          name: 'Restautant La Martinière',
          location: '13 rue Victor Henrri Saint Martin de Ré'
        },
        {
          thumbnail: require('../../assets/images/restaurant4.png'),
          name: 'Restautant pot d\'etain',
          location: '13 rue Victor Henrri Saint Martin de Ré'
        }
      ]
    }
  }
}
</script>

<style lang='scss'>
  .restaurant {
    padding-top: 146px;
    @include on('mobile') {
      padding: 16px 0;
    }
    &__header {
      margin-bottom: 58px;
      @include on('mobile') {
        margin-bottom: 16px;
      }
    }
  }
</style>
