<template>
  <vs-card class="rescard">
    <template #title>
      <h3 class="rescard__title">
        {{ name }}
      </h3>
    </template>
    <template #img>
      <img :src="thumbnail" alt="Restaurant Image">
    </template>
    <template #text>
      <p class="rescard__location">
        <map-pin-icon class="rescard__location-icon" />
        <span class="rescard__location-text">{{ location }}</span>
        <span class="rescard__location-dot" />
      </p>
      <div v-if="type === 'appartment'" class="rescard__specs">
        <div class="rescard__spec">
          <i class="bx bx-bed" />
          <p> {{ bedroom }} </p>
        </div>
        <div class="rescard__spec">
          <i class="bx bx-bath" />
          <p> {{ bathroom }} </p>
        </div>
        <div class="rescard__spec">
          <i class="bx bx-dollar" />
          <p> {{ cost }} </p>
        </div>
      </div>
      <div v-else-if="type === 'restaurant'" class="rescard__specs">
        <div class="rescard__spec">
          <i class="bx bx-bed" />
          <p>Française</p>
        </div>
        <div class="rescard__spec">
          <i class="bx bx-bath" />
          <p>Déjeuner, Dîner</p>
        </div>
      </div>
      <vs-button size="xl" class="c-button rescard__reserve">
        Réserver
      </vs-button>
    </template>
  </vs-card>
</template>

<script>
import { MapPinIcon } from 'vue-feather-icons'
export default {
  name: 'ReserveCard',
  components: {
    MapPinIcon
  },
  props: {
    type: {
      type: String,
      default: 'appartment'
    },
    thumbnail: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    location: {
      type: String,
      required: true
    },
    bedroom: {
      type: [Number, String],
      default: 0
    },
    bathroom: {
      type: [Number, String],
      default: 0
    },
    cost: {
      type: [Number, String],
      default: 0
    }
  }

}
</script>

<style lang='scss'>
  .rescard {
    &__title {
      @include font(22px, 25px, #112884, bold)
    }
    &__location {
      display: flex;
    }
    &__location-text {
      max-width: 158px;
    }
    &__location-icon {
      height: 13px;
      width: 10.64px;
      margin-right: 4px
    }
    &__location-dot {
      @include circle(9px);
      background-color: #27EF35;
      margin-top: 3px;
      margin-left: 3px;
    }
    &__specs {
      display: flex;
      margin: 16px 0;
    }
    &__spec {
      display: flex;
      align-items: center;
      height: 28px;
      &:not(:last-child){
        border-right: 1px solid rgba(#112884, 0.15);
      }
      &:not(:first-child){
        padding: 0 24px;
      }
      &:first-child {
        padding-right: 24px;
      }
      &:last-child {
        padding-right: 0;
      }
      i {
        font-size: 20px;
        color: #909BC5;
        margin-right: 12px;
      }
      p {
        @include font(18px, 20px, #112884, 500)
      }
    }

    &__reserve {
      width: 100%;
      background-color: #3B96D2;
    }

    .vs-card {
      box-shadow: none;
      border-radius: 20px 0;
      border: 1px solid #E5E5E5;
      overflow: hidden;
    }
    .vs-card__title {
      padding: 16px 0;
    }
    .vs-card__text {
      padding: 0 20px;
      padding-bottom: 20px;
    }
    .vs-card__img,
    .vs-card__img img {
      border-radius: 0 !important;
    }
  }
</style>
