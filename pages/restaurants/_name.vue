<template>
  <div class="res">
    <div class="res__left">
      <vs-breadcrumb class="res__bread" :items="breadcrumb" separator="arrow_right" />
      <vs-row>
        <vs-col vs-w="8">
          <div class="res__details">
            <vs-row>
              <vs-col vs-w="3">
                <vs-images class="res__images has-margin">
                  <li
                    v-for="image in images"
                    :key="image.id"
                    :src="image.src"
                    :class="{active: active === image.id}"
                    class="vs-image res__image"
                    @click="active = image.id"
                  >
                    <div class="con-vs-image">
                      <div
                        class="vs-image--img"
                        :style="`background-image: url('${image.src}');`"
                      />
                    </div>
                    <img
                      :src="image.src"
                      class="imag-blur"
                    >
                  </li>
                </vs-images>
                <div class="res__info">
                  <p>Ouvert<br>Aujourd'hui</p>
                  <span>
                    dans une heure
                    <i class="bx bx-info-circle" />
                  </span>
                </div>
              </vs-col>
              <vs-col vs-w="9">
                <vs-images hover="zoom" class="res__images">
                  <vs-image
                    :src="activeImage"
                    class="res__image-preview"
                  />
                </vs-images>
                <div class="res__header">
                  <div class="res__heading">
                    <h3 class="res__title">
                      Restaurant au pot d'etain
                    </h3>
                    <p class="res__subtitle">
                      Saint-Martin-de-Ré
                    </p>
                  </div>
                  <div class="res__header-icons">
                    <vs-tooltip text="Partage">
                      <vs-button radius type="flat" icon="reply" />
                    </vs-tooltip>
                    <vs-tooltip text="Favorite">
                      <vs-button radius type="flat" color="danger" icon="favorite" />
                    </vs-tooltip>
                    <vs-tooltip text="More">
                      <vs-button radius type="flat" icon="more_horiz" />
                    </vs-tooltip>
                  </div>
                </div>
              </vs-col>
            </vs-row>
          </div>
        </vs-col>
        <vs-col vs-w="4">
          <div class="res__card">
            <div class="res__card-header">
              <div class="res__card-thumb">
                <img src="../../assets/images/res-thumb.png">
              </div>
              <div class="res__card-desc">
                <h5 class="res__card-header-title">
                  Patrick Léo
                </h5>
                <p class="flex align-center">
                  <i class="res__card-star bx bxs-star" />
                  <strong class="res__card-rating">4.79</strong>
                  <span class="res__card-comment">(95 Commentaires)</span>
                </p>
              </div>
            </div>
            <hr class="res__card-divider">
            <div class="res__card-form">
              <vs-input icon-no-border icon="today" label="Dates" value="01/10/20 -> 12:00" />
              <vs-select
                label="Figuras"
                class="selectExample"
                placeholder="4 Invites"
              >
                <vs-select-item value="1" text="4 Invites" />
              </vs-select>
              <vs-button color="primary" type="filled" size="large" class="c-button w-100">
                Reserver
              </vs-button>
            </div>
          </div>
        </vs-col>
      </vs-row>
      <vs-row>
        <vs-col vs-w="2">
          <div class="res__iconbar">
            <vs-button radius size="large" type="flat">
              <i class="vs-icon icon-scale vs-button--icon bx bxs-offer" />
            </vs-button>
            <vs-button radius size="large" type="flat" class="isActive">
              <i class="vs-icon icon-scale vs-button--icon bx bx-info-circle" />
            </vs-button>
            <vs-button radius size="large" type="flat">
              <i class="vs-icon icon-scale vs-button--icon bx bx-calendar" />
            </vs-button>
            <vs-button radius size="large" type="flat">
              <i class="vs-icon icon-scale vs-button--icon bx bx-wallet" />
            </vs-button>
            <vs-button radius size="large" type="flat">
              <i class="vs-icon icon-scale vs-button--icon bx bx-door-open" />
            </vs-button>
            <vs-button radius size="large" type="flat">
              <i class="vs-icon icon-scale vs-button--icon bx bx-star" />
            </vs-button>
          </div>
        </vs-col>
        <vs-col vs-w="6">
          <div class="res__desc">
            <hr class="res__desc-divider">
            <vs-row>
              <vs-col vs-w="4">
                <div class="res__desc-subheader">
                  Cuisine
                </div>
                <div class="res__desc-text hm">
                  Française
                </div>
              </vs-col>
              <vs-col vs-w="4">
                <div class="res__desc-subheader">
                  Capacité
                </div>
                <div class="res__desc-text hm">
                  Capacité
                </div>
              </vs-col>
              <vs-col vs-w="4">
                <div class="res__desc-subheader">
                  Salles
                </div>
                <div class="res__desc-text hm">
                  1
                </div>
              </vs-col>
            </vs-row>
            <vs-row>
              <vs-col vs-w="4">
                <div class="res__desc-subheader">
                  Repas
                </div>
                <div class="res__desc-text">
                  Déjeuner, Dîner
                </div>
              </vs-col>
              <vs-col vs-w="4">
                <div class="res__desc-subheader">
                  Equipements
                </div>
                <div class="res__desc-text">
                  Terrasse
                </div>
              </vs-col>
              <vs-col vs-w="4">
                <div class="res__desc-subheader">
                  Taux d'occupation
                </div>
                <div class="res__desc-rating">
                  <span />
                  <span />
                  <span />
                  <span />
                  <span />
                  <span />
                </div>
              </vs-col>
            </vs-row>
            <hr class="res__desc-divider">
            <h4 class="res__desc-title">
              Déscription
            </h4>
            <p class="res__desc-desc">
              Le Pot d’Étain, dans un cadre rustique et une ambiance familiale, situé au cœur de Saint-Martin de Ré, vous accueille toute l'année depuis 1969.
              Crêperie et restaurant traditionnel (grillades, salades, poissons).<br><br>

              Le Pot d’Étain utilise des produits de l'île de Ré : fromage de chèvre de Loix, apéritif vin de Ré, pétillant trousse-chemise, pommes de terre de l'île...
              Crêpes au sarrasin, cuisine sans gluten (sauf pour les crêpes).<br><br>

              Ouvert toute l'année.
              Fermé le mardi (hors vacances scolaires) et 7j/7 en juillet/août et pendant les vacances scolaires.
            </p>
          </div>
        </vs-col>
        <vs-col vs-w="4">
          <div class="res__desc-contact">
            <div>
              <h6>
                Téléphone
                <i class="bx bx-phone-call" />
              </h6>
              <p>+33 (0)1  23 45 67 89</p>
            </div>
            <div>
              <h6>
                Site web
                <i class="bx bx-world" />
              </h6>
              <p>www.potetain.fr</p>
            </div>
            <div>
              <h6>
                Menu
                <i class="bx bx-dish" />
              </h6>
              <p>Voir le menu</p>
            </div>
          </div>
        </vs-col>
      </vs-row>
    </div>
    <div class="res__map">
      <iframe
        frameborder="0"
        style="border:0"
        allowfullscreen
        src="https://www.google.com/maps/embed/v1/place?key=AIzaSyA-10-OHpfss9XvUDWILmos62MnG_L4MYw
          &q=Space+Needle,Seattle+WA"
      />
      <div class="res__map-expander relative circle">
        <div class="center">
          <i class="bx bx-chevrons-left" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Restaurant',
  layout: 'nofooter',
  data () {
    return {
      breadcrumb: [
        {
          title: 'Accueil',
          url: '/'
        },
        {
          title: 'Restaurants',
          url: '/restaurants'
        },
        {
          title: this.name,
          active: true
        }
      ],
      active: 1,
      images: [
        {
          id: 1,
          src: require('../../assets/images/res1.png')
        },
        {
          id: 2,
          src: require('../../assets/images/res2.png')
        },
        {
          id: 3,
          src: require('../../assets/images/res3.png')
        }
      ]
    }
  },
  computed: {
    activeImage () {
      return this.images.find(({ id }) => id === this.active).src
    }
  },
  created () {
    this.breadcrumb[this.breadcrumb.length - 1].title = this.$route.params.name.split('-').join(' ')
  }
}
</script>

<style lang='scss'>
  .res {
    position: relative;
    padding-left: 53px;
    display: flex;
    &__left {
      flex: 1;
    }
    &__bread {
      padding: 27px 0;
      ol {
        padding: 0;
      }
    }

    // Start Map
    &__map {
      width: 392px;
      height: 100vh;
      position: relative;
      iframe {
        width: 100%;
        height: 100%;
        min-height: 1000px;
      }
    }
    &__map-expander {
      cursor: pointer;
      position: absolute;
      left: -35px; top: 70%;
      transform: translateY(-50%);
      @include rect(71px);
      border: 1px solid #D8E6DB;
      background-color: white;
      box-shadow: 0 3px 6px rgba(#000000, 0.016);
      i {
        font-size: 28px;
        color: #C4C4C4;
      }
    }
    // End Map

    &__images {
      flex-direction: column;
      &.has-margin {
        margin-right: 20px;
      }
    }
    &__image,
    &__image-preview {
      width: 100%;
    }
    &__image {
      border: 2px solid transparent;
      transition: border 300ms ease-in-out;
      &.active {
        transform: none !important;
        .con-vs-image {
          transform: scale(0.95);
        }
        border-color:#3965de;
      }
      .con-vs-image {
        height: 140px;
      }
    }
    &__image-preview {
      .con-vs-image {
        height: 436px;
      }
    }
    &__info {
      margin-top: 40px;
      p {
        margin-bottom: 4px;
        @include font(18px, 22px, #10B859, bold);
      }
      span {
        display: flex;
        align-items: center;
        @include font(16px, 18px, #7E8989);
        i {
          margin-left: 12px;
        }
      }
    }

    // Start Header
    &__header {
      display: flex;
      margin-top: 40px;
      justify-content: space-between;
    }
    &__title {
      margin-bottom: 8px;
      @include font(35px, 40px, #223263, bold);
    }
    &__subtitle {
      margin-bottom: 48px;
      @include font(16px, 18px, #7E8989, 500);
    }
    &__header-icons {
      display: flex;
      > div {
        margin-right: 8px;
      }
    }
    // End Header

    // Start Desc

    &__desc-divider {
      border: none;
      height: 1px;
      background-color: #E8EBE9;
      margin-bottom: 48px;
    }

    &__desc-subheader {
      margin-bottom: 8px;
      @include font(16px, 18px, #7E8989)
    }

    &__desc-text {
      margin-bottom: 28px;
      @include font(20px, 22px, #223263, 600);
    }
    &__desc-title {
      margin-bottom: 27px;
      @include font(24px, 27px, #223263, 600)
    }
    &__desc-desc {
      margin-bottom: 44px;
      @include font(14px, 25px,#7E8989)
    }
    // End Desc

    // Start Desc Contact

    &__desc-contact {
      margin-left: 24px;
      margin-top: 44px;
      h6 {
        margin-bottom: 12px;
        @include font(19px, 30px,#223263, 700)
      }
      i {
        color: #7E8989;
        font-size: 16px;
      }
      p {
        margin-bottom: 24px;
        @include font(16px, 18px,#7E8989)
      }
    }
    // End Desc Contact

    // Start IconBar
    &__iconbar {
      padding: 16px;
      display: flex;
      width: max-content;
      border-radius: 44px;
      flex-direction: column;
      background-color: #F2F5F3;
      button:not(:last-child) {
        margin-bottom: 12px;
      }
      button {
        width: 44px;
        height: 44px;
      }
      button.isActive {
        background-color: #3B96D2 !important;
      }
      .vs-icon {
        color: #7E8989;
        font-size: 20px;
      }
    }
    // End Start IconBar

    // Start Res Card
    &__card {
      width: 398px;
      padding: 30px;
      margin: 0 auto;
      border: 1px solid #D8E6DB;
      border-radius: 12px;
    }
    &__card-header {
      display: flex;
      align-items: center;
    }
    &__card-thumb {
      @include rect(54px);
      margin-right: 10px;
    }
    &__card-header-title {
      // margin-bottom: 12px;
      @include font(19px, 34px, #484848, 500)
    }
    &__card-star {
      color: #FFC701;
    }
    &__card-rating {
      @include font(14px, 28px, #484848)
    }
    &__card-star,
    &__card-rating {
      margin-right: 4px;
    }
    &__card-comment {
      @include font(14px, 28px, #767676)
    }
    &__card-divider {
      margin: 16px 0;
    }
    &__card-form {
      .vs-con-input-label,
      .con-select {
        width: 100%;
        margin-bottom: 22px;
      }
      .vs-input {
        margin-bottom: 14px;
      }
      .vs-input--input,
      .vs-select--input {
        height: 48px;
        border-color: #D8E6DB !important;
        @include font(18px, 38px, #484848)
      }
      .vs-input--icon {
        top: 50%;
        transform: translateY(-50%);
      }
      .vs-select--label,
      .vs-input--label {
        @include font(12px, 24px, #484848)
      }
    }
    // End Res Card

    .vs-image--img {
      background-position: center;
      background-size: cover;
      background-repeat: no-repeat;
    }
    .vs-images--ul {
      padding: 0;
    }
  }
</style>
