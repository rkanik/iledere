<template>
  <div class="explore">
    <ImageSection  />
    <Presentation class="section-padding section-padding-top"  />
    <Slider class="section-padding-bottom section-padding-top"  />
    <Activities class="section-padding-bottom" />
    <Histoire  class="section-padding-bottom" />
  </div>
</template>

<script>
import ImageSection from '@/components/Explore/ImageSection'
import Presentation from '@/components/Explore/Presentation'
import Slider from '@/components/Explore/Slider'
import Histoire from '@/components/Explore/Histoire'
import Activities from '@/components/Explore/Activities'
export default {
  components: {
    ImageSection,Presentation,Histoire,Activities,Slider
  }
}
</script>
<style lang='scss' scoped>
    .section-padding-bottom{
      padding-bottom: 120px;
    }
    .section-padding-top{
      padding-top: 120px;
    }

</style>
