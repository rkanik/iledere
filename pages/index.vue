<template>
  <div class="home">
    <HeroSection />
    <AboutSection />
    <HebergementSection />
    <RestaurantsSection />

    <div class="container">
      <div class="map">
        <h2 class="map__title">
          île de ré
        </h2>
        <div class="map__bg">
          <img src="../assets/images/home-map.png" alt="" class="map__map">
        </div>
      </div>
    </div>

    <div class="container">
      <div class="mobapp">
        <vs-row vs-w="12" vs-align="center" vs-justify="space-between">
          <vs-col vs-w="6">
            <div class="mobapp__subheader">
              APPLICATION MOBILE
            </div>

            <h2 class="mobapp__title">
              Réapp est disponible sur les stores Google Play & App Store
            </h2>

            <p class="mobapp__content">
              Meet artists with various art styles and concepts, and explore the inspiration and process behind their work. Learn methods to create quality art and star up business.
            </p>

            <div class="mobapp__link-title">
              Télécharger l'application
            </div>

            <div class="mobapp__link-images">
              <img src="../assets/images/applestore.png" class="mobapp__link-image">
              <img src="../assets/images/googleplay.png" class="mobapp__link-image">
            </div>
          </vs-col>
          <vs-col vs-w="4">
            <div class="mobapp__image">
              <img src="../assets/images/home-phone.png">
            </div>
          </vs-col>
        </vs-row>
      </div>
    </div>
  </div>
</template>

<script>

// Sections
import HeroSection from '@/components/Home/HeroSecton'
import AboutSection from '@/components/Home/AboutSection'
import HebergementSection from '@/components/Home/HebergementSection'
import RestaurantsSection from '@/components/Home/RestaurantsSection'

export default {
  components: {
    HeroSection,
    AboutSection,
    HebergementSection,
    RestaurantsSection
  }
}
</script>

<style lang='scss' scoped>
  .map {
    padding: 140px 0;
    &__title {
      @include font(43px, 48px, #223263, 600)
    }
    &__bg {
      background: linear-gradient(
        to bottom,
        white 0%,
        #F5F6F6 100%,
      );
      border-radius: 73px;
    }
  }
  .mobapp {
    padding-bottom: 140px;
    &__subheader {
      @include font(16px, 80px, rgba(black, 0.7))
    }
    &__title {
      @include font(40px, 49px, #223263, 600);
      margin-bottom: 32px;
    }
    &__content {
      @include font(18px, 36px, rgba(black, 0.8));
      margin-bottom: 40px;
    }
    &__link-title {
      @include font(37px, 81px, #3B96D2);
      margin-bottom: 32px;
    }
  }
</style>
