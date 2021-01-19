<template>
  <div class='container'>
    <vs-row vs-w="12">
      <vs-col vs-lg="6" vs-sm="12" vs-xs="12">
        <div class='image'>
          <p class='image__text'>HISTOIRE</p>
          <img src="../../assets/images/history.png">
        </div>
      </vs-col>
      <vs-col vs-justify="center" vs-align="center" vs-lg="6" vs-sm="12" vs-xs="12">
        <div class='text'>
          <p class='text__title'>Histoire de l'île de Ré</p>
          <p class='text__content'>Après la quatrième période glaciaire, l’Île de Ré se détacha du continent. Elle se
            composait alors de quatre îles : Les Portes, Ars, Loix et Ré. Lentement, ces quatre îlots se sont rattachés
            grâce au travail de la Nature, aidés de la main de l’Homme pour donner cette forme d’hippocampe.</p>
        </div>
        <div class='collapse-content'>
          <vs-collapse accordion>
            <vs-collapse-item icon-arrow="add">
              <div class='collapse-content__header' slot="header">
                Des vestiges
              </div>
              <div class='collapse-content__content'>
                De l’habitat préhistorique et gallo romains ont été retrouvés
                dans le centre de l’île. Au Moyen-Âge, Ré était vouée à
                l’agriculture. Les premiers seigneurs de Ré.. voir plus
              </div>
            </vs-collapse-item>
            <vs-collapse-item icon-arrow="add">
              <div class='collapse-content__header' slot="header">
                L'île de Ré
              </div>
              <div class='collapse-content__content'>
                De l’habitat préhistorique et gallo romains ont été retrouvés
                dans le centre de l’île. Au Moyen-Âge, Ré était vouée à
                l’agriculture. Les premiers seigneurs de Ré.. voir plus
              </div>
            </vs-collapse-item>
            <vs-collapse-item icon-arrow="add">
              <div class='collapse-content__header' slot="header">
                L'île de Ré
              </div>
              <div class='collapse-content__content'>
                De l’habitat préhistorique et gallo romains ont été retrouvés
                dans le centre de l’île. Au Moyen-Âge, Ré était vouée à
                l’agriculture. Les premiers seigneurs de Ré.. voir plus
              </div>
            </vs-collapse-item>
            <vs-collapse-item icon-arrow="add">
              <div class='collapse-content__header' slot="header">
                Ré
              </div>
              <div class='collapse-content__content'>
                De l’habitat préhistorique et gallo romains ont été retrouvés
                dans le centre de l’île. Au Moyen-Âge, Ré était vouée à
                l’agriculture. Les premiers seigneurs de Ré.. voir plus
              </div>
            </vs-collapse-item>
          </vs-collapse>
        </div>
      </vs-col>
    </vs-row>

  </div>
</template>

<style lang='scss' scoped>
  .image {
    margin-left: auto;
    margin-right: auto;

    &__text {
      @include font(28px, 41px, #363636);
      padding: 8px 0;
    }
  }

  .text {
    padding-left: 100px;

    &__title {
      padding-top: 10px;
      @include font(46px, 104px, #223263, bold);
    }

    &__content {
      @include font(24px, 30px);
    }
  }

  .collapse-content {
    padding-top:60px;
    padding-left: 84px;

    &__header {
      @include font(26px, 59px, #223263, bold);
    }
    &__content {
      @include font(24px, 35px, #707070);
      padding:32px;
    }
  }
</style>
