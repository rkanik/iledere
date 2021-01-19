<template>
 <div class='Image'>
   <div class='Image__content'>
    <span class='Image__title'>L'île de ré un des meilleurs destinations </span><br>
    <span class='Image__subtitle'>Découvez l'île de Ré</span>
   </div>
       <WeatherCard class="hero__weather" />
 </div>

</template>

<script>
import WeatherCard from '@/components/WeatherCard'
export default {
  components: {
    WeatherCard
  }
}
</script>

<style lang='scss' scoped>
  .Image {
    min-height: 985px;
    background-image: url(../../assets/images/destination.png);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center ;
    position: relative;
    &__content {
      position: absolute;
      top: 50%;
      left: 40%;
      color:white;
      transform: translate(-50%, -50%)
    }
    &__title {
     font-size:93px
    }
    &__subtitle{
      font-size: 33px;
      border-bottom: 4px solid;
      padding: 10px;
    }
  }

</style>
