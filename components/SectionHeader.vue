<template>
  <div class="sechead">
    <h2 class="sechead__title">
      {{ title }}
      <span class="sechead__count">
        ({{ count }})
      </span>
    </h2>
    <div class="sechead__more">
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

<style lang='scss' scoped>
  .sechead {
    display: flex;
    justify-content: space-between;
    align-items: center;
    &__title {
      @include font(46px, 104px, #223263, bold)
    }
    &__count {
      @include font(40px, 105px, #223263)
    }
    &__more {
      @include font(17px, 94px, #112884);
      cursor: pointer;
      display: flex;
      align-items: center;
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
