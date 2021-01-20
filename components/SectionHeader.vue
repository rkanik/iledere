<template>
  <div class="sechead">
    <h2 class="sechead__title">
      {{ title }}
      <span class="sechead__count">
        ({{ count }})
      </span>
    </h2>
    <div class="sechead__more hon-mobile">
      {{ more }}
      <i class="bx bx-arrow-back" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionHeader',
  props: {
    title: {
      type: String,
      required: true
    },
    count: {
      type: [Number, String],
      required: true
    },
    more: {
      type: String,
      default: 'Voir plus'
    }
  }
}
</script>

<style lang='scss'>
  .sechead {
    display: flex;
    justify-content: space-between;
    align-items: center;
    &__title {
      @include font(46px, 104px, #223263, bold);
      @include on('mobile'){
        @include font(27px, 61px, #223263, bold);
      }
    }
    &__count {
      @include font(40px, 105px, #223263);
      @include on('mobile'){
        @include font(22px, 60px, #223263);
      }
    }
    &__more {
      @include font(17px, 94px, #112884);
      cursor: pointer;
      display: flex;
      align-items: center;
      @include on('mobile'){
        justify-content: center;
        @include font(14px, 16px, #112884);
      }
      i {
        font-size: 22px;
        margin-left: 16px;
        transition: transform 300ms ease-in-out;
        transform: rotate(180deg);
      }
      &:hover i {
        transform: rotate(180deg) translateX(-8px);
      }
    }
  }
</style>
