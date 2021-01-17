<template>
  <div class="about">
    <div class="container">
      <vs-row>
        <vs-col
          vs-type="flex"
          vs-justify="center"
          vs-align="center"
          w="7"
        >
          <div class="about__divider" />
          <h2 class="about__title">
            The domn ohickey Company was founded in this stpey
            has been providing quality doohickeys to the public
            ever since.
          </h2>
          <p class="about__content">
            L’île de Ré, reliée au continent par un pont a une superficie de 85 km2 et une longueur de 32 kilomètres. Sa largeur varie de 5 kilomètres à 100 mètres à peine, au passage du Martray. Dans les terres, découvrez à vélo les vignes, les champs exploités puis plus au Nord, la magie des marais salants.<br><br>
            Le long des dix villages, partez à la découverte du patrimoine, des ports et de la riche histoire insulaire. Le littoral présente des aspects très différents : dunes, petites falaises, rochers, longues plages de sable fin ...
          </p>

          <vs-button size="xl" class="c-button savoir-button">
            En savoir plus
          </vs-button>
        </vs-col>
        <vs-col
          vs-type="flex"
          vs-justify="center"
          vs-align="center"
          w="5"
        >
          <div class="about__image">
            <img src="../../assets/images/about.png">
          </div>
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>
<script>
export default {
  name: 'AboutSection'
}
</script>
<style lang="scss">
  .about {
    padding: 123px 0 85px 0;
    &__divider {
      height: 2px;
      width: 119.82px;
      background-color: #3965DE;
      margin-bottom: 36px
    }
    &__title {
      @include font(35px, 51px, #3B96D2);
      margin-bottom: 55px;
      max-width: 862px;
    }
    &__content {
      @include font(20px, 36px, #223263);
      max-width: 710px;
      margin-bottom: 54px;
    }
    &__image {
      width: 551px;
      height: 576px;
      margin-top: 97px;
      border-radius: 20px 0;
      background-color: #F6F8FD;
      img {
        transform: translate(-83px, 85px);
        transition: transform 300ms ease-in-out;
        &:hover {
          transform: translate(-63px, 65px);
        }
      }
    }
    .savoir-button {
      background-color: #3B96D2;
    }
  }
</style>
