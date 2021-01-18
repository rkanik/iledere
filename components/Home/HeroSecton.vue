<template>
  <div class="hero">
    <div class="hero__content">
      <h1 class="hero__title">
        L'île de ré un des meilleurs destinations.
      </h1>
      <div class="hero__tabs">
        <div size="xl" class="hero__tab active">
          Je m'informe
        </div>
        <div size="xl" class="hero__tab">
          Je réserve
        </div>
      </div>
      <div class="hero__form">
        <vs-row vs-w="12" class="hero__form-row">
          <vs-col vs-w="3">
            <label>Activité</label>
            <vs-select v-model="value" placeholder="Artisant">
              <vs-select-item
                v-for="opt in options"
                :key="opt.value"
                :text="opt.text"
                :value="opt.value"
              />
            </vs-select>
          </vs-col>
          <vs-col vs-w="3">
            <label>Catégorie</label>
            <vs-select v-model="value" placeholder="Maçon">
              <vs-select-item
                v-for="opt in options"
                :key="opt.value"
                :text="opt.text"
                :value="opt.value"
              />
              </vs-select-item>
            </vs-select>
          </vs-col>
          <vs-col vs-w="3">
            <label>Commune</label>
            <vs-select v-model="value" placeholder="La noue">
              <vs-select-item
                v-for="opt in options"
                :key="opt.value"
                :text="opt.text"
                :value="opt.value"
              />
            </vs-select>
          </vs-col>
          <vs-col vs-w="3">
            <label>NOM</label>
            <vs-input v-model="value" placeholder="Recherche" />
          </vs-col>
        </vs-row>
        <div class="hero__search">
          <i class="bx bx-search" />
        </div>
      </div>
    </div>
    <div class="hero__slider">
      <div class="hero__slide">
        <i class="bx bx-chevron-up" />
      </div>
      <div class="hero__slider-indicator" />
      <div class="hero__slide active">
        <i class="bx bx-chevron-down" />
      </div>
    </div>
    <WeatherCard class="hero__weather" />
    <div class="hero__watch">
      <div class="hero__watch-play">
        <i class="bx bx-play" />
      </div>
      <div class="hero__watch-title">
        Watch Promo
      </div>
    </div>
  </div>
</template>

<script>
import WeatherCard from '@/components/WeatherCard'
export default {
  name: 'Hero',
  components: {
    WeatherCard
  },
  data: () => ({
    value: '',
    options: [
      { text: 'Vue', value: 1 },
      { text: 'Vuesax', value: 2 },
      { text: 'Javascript', value: 3 },
      { text: 'Typescript', value: 4 }
    ]
  })

}
</script>

<style lang='scss'>
  .hero {
    min-height: 985px;
    background-image: url(../../assets/images/hero.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center ;
    position: relative;
    &__content {
      margin: 0 auto;
      max-width: 1192px;
      padding-top: 320px;
    }
    &__title {
      @include font(96px, 111px, white, bold);
      margin-bottom: 82px;
      max-width: 1012px;
    }
    &__tabs {
      display: flex;
    }
    &__tab {
      height: 80px;
      width: 327px;
      padding: 24px 0;
      cursor: pointer;
      text-align: center;
      background-color: white;
      @include font(20px, 32px, #223263, bold);
      border-bottom: 1px solid #F0EBEB;
      &.active {
        background-color: #3B96D2;
        color: white;
      }
      &:first-child {
        border-top-left-radius: 6px;
      }
      &:last-child {
        border-top-right-radius: 6px;
      }
    }
    &__form {
      background-color: white;
      border-radius: 6px;
      border-top-left-radius: 0;
      display: flex;
      align-items: center;
      label:not(.vs-select__label, .vs-input__label) {
        margin-bottom: 16px;
        display: inline-block;
        text-transform: uppercase;
        @include font(15px, 17px, #A8A9AA, bold);
      }

      .vs-select--input,
      .vs-input--input {
        border: none !important;
        background-color: white;
        padding-left: 0;
        border-radius: 0;
        border-bottom: 1px solid #F0EBEB !important;
      }
      .vs-input-primary .vs-input--input:focus {
        border: none !important;
        box-shadow: none !important;
        border-bottom: 1px solid #F0EBEB !important;
      }
      .vs-select--icon {
        color: #A8A9AA !important;
        font-size: 20px !important;
      }
      .vs-select--input::placeholder,
      .vs-input--placeholder {
        @include font(17px, 19px, #3B96D2);
      }
      .vs-input {
        height: 38px;
      }
      .con-select {
        max-width: unset;
      }
      .vs-col:not(:last-child) {
        padding-right: 16px;
      }
    }
    &__form-row {
      padding: 16px 0 16px 75px;
    }
    &__search {
      width: 104px;
      height: 104.16px;
      display: flex;
      background-color: #3B96D2;
      border-top-right-radius: 6px;
      border-bottom-right-radius: 6px;
      justify-content: center;
      align-items: center;
      color: #EBF0FF;
      font-size: 36px;
      cursor: pointer;
      transition: background-color 300ms ease-in-out;
      &:hover {
        background-color: rgb(59, 169, 243)
      }
    }
    &__slider {
      display: flex;
      flex-direction: column;
      align-items: center;
      position: absolute;
      left: 72px;
      top: 50%;
      transform: translateY(-50%);
    }
    &__slide {
      display: flex;
      font-size: 24px;
      border: 1px solid white;
      justify-content: center;
      cursor: pointer;
      color: white;
      align-items: center;
      @include circle(48px);
      transition: all 300ms ease-in-out;
      &.active, &:hover {
        border-color: #3B96D2;
        background-color: #3B96D2;
      }
    }
    &__slider-indicator {
      width: 2px;
      margin: 48px 0;
      height: 360px;
      border-radius: 16px;
      position: relative;
      background-color: #EBF0FF;
      &::before {
        content: '';
        display: block;
        width: 100%;
        height: 71px;
        background-color: #3B96D2;
        position: absolute;
        bottom: 0;
        left: 0;
      }
    }
    &__weather {
      position: absolute;
      top: 64px;
      right: 140px;
    }
    &__watch {
      display: flex;
      align-items: center;
      position: absolute;
      top: 50%;
      right: 0;
      transform: translateY(-50%) rotate(-90deg);
    }
    &__watch-title {
      @include font(18px, 20px, #F4F5F7);
      margin-left: 24px;
    }
    &__watch-play {
      display: flex;
      @include circle(48px);
      background-color: white;
      justify-content: center;
      align-items: center;
      font-size: 24px;
      color: #3B96D2;
      transform: rotate(90deg);
      cursor: pointer;
    }
  }
</style>
