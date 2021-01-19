<template>
  <div class='container'>
    <vs-row vs-w="12">
      <vs-col vs-justify="center" vs-align="center" vs-lg="6" vs-sm="12" vs-xs="12">
        <div class='text'>
         <p class='text__title'>UN PARADIS D'ACTIVITÉS</p>
         <p class='text__subtitle'>Un large panel d’activités est proposé aux adultes et aux enfants, tout au long de l’année.</p>
         <p class='text__content'>Arrivent en tête : voile, kite surf, planche...mais on peut aussi bien jouer au golf
           aux Portes en Ré, au tennis dans chaque village, monter à cheval et parcourir les plages. Les familles vont
           être comblées par tous ces ateliers de découvertes proposés aux enfants, ainsi qu’aux parents :</p>
         <br>
         <p class='text__content'>ballades historiques dans les communes, promenades en mer, découvertes du patrimoine
           bâti ou vivant.</p>
          <div class="text__border">
            <span class="text__border-text" >Les Activités Nautiques</span>
          </div>
          <div class="text__icon">
            <i></i>
          </div>

        </div>
      </vs-col>
      <vs-col vs-lg="6" vs-sm="12" vs-xs="12">
        <div class='image'>
          <img src="../../assets/images/activities.png">
        </div>
      </vs-col>
    </vs-row>

  </div>
</template>

<style lang='scss' scoped>
  .image {
    position: relative;
    margin-left: auto;
    margin-right: auto;

    &__text {
      @include font(28px, 41px, #363636);
      padding: 8px 0;
    }
    img{
      // position: ;
      // overflow: hidden;
    }
  }


  .text{
    padding-top:16px;
    padding-right:100px;
    &__title {
        font-size:28px;
        color: #3B96D2;
        padding-bottom:15px;
    }
    &__subtitle {
       @include font(35px, 51px,normal);
       padding-right:37px;
    }
    &__content {
       padding-top:28px;
       @include font(20px, 36px);
    }
    &__border{
      padding-top: 100px;
      @include font(32px, 44px);
    }
    &__border-text{
      padding-bottom: 18px;
      border-bottom: 3px solid #B7B7B7;
    }
  }
</style>
