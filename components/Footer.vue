<template>
  <div class="footer">
    <div class="container">
      <div class="footer__top">
        <vs-row>
          <vs-col w="3">
            <h4 class="footer__title">
              île de ré
            </h4>
            <div class="footer__links">
              <NuxtLink to="#" class="footer__link">
                Explorer L'ile
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Se Loger
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Que faire sur l'ile
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Savoure
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Vie Quotidienne
              </NuxtLink>
            </div>
          </vs-col>
          <vs-col w="3">
            <h4 class="footer__title">
              Communauté
            </h4>
            <div class="footer__links">
              <NuxtLink to="#" class="footer__link">
                Top Hébergement
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Top Restaurants
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Top Activités
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Top Évenements
              </NuxtLink>
              <NuxtLink to="#" class="footer__link">
                Politique de confidentialité
              </NuxtLink>
            </div>
          </vs-col>
          <vs-col w="3">
            <h4 class="footer__title">
              Contact
            </h4>
            <div class="footer__contact">
              <p class="footer__address">
                Addresse : 165, Lorem ipsum, France<br>7853
              </p>
              <p class="footer__phone">
                Téléphone : +33 012345678
              </p>
              <p class="footer__email">
                Email : réapp@info.fr
              </p>
            </div>
          </vs-col>
          <vs-col w="3">
            <NuxtLink to="/" class="footer__brand-logo">
              <div>
                <img src="../assets/images/logo.png" alt="Brand Logo">
                <div class="footer__brand-name">
                  île de ré
                </div>
              </div>
              <div class="footer__go-top" @click="gotoTop">
                <i class="bx bx-up-arrow-alt" />
              </div>
            </NuxtLink>
            <div class="footer__newsletter">
              <div class="footer__newsletter-title">
                Abonnez-nous!
              </div>
              <div class="footer__newsletter-form">
                <vs-input placeholder="Déposez votre e-mail" class="footer__newsletter-input" />
                <vs-button icon class="footer__newsletter-button">
                  <i class="bx bxs-paper-plane" />
                </vs-button>
              </div>
            </div>
          </vs-col>
        </vs-row>
      </div>
    </div>
    <hr class="footer__divider">
    <div class="container">
      <div class="footer__bottom">
        <div class="footer__copyright">
          2020 @ Tous droits réservés par Réapp.
        </div>
        <div class="footer__social-links">
          <NuxtLink to="#" class="footer__social-link">
            <i class="bx bxl-facebook" />
          </NuxtLink>
          <NuxtLink to="#" class="footer__social-link">
            <i class="bx bxl-twitter" />
          </NuxtLink>
          <NuxtLink to="#" class="footer__social-link">
            <i class="bx bxl-linkedin" />
          </NuxtLink>
          <NuxtLink to="#" class="footer__social-link">
            <i class="bx bxl-instagram" />
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  methods: {
    gotoTop () {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: 'smooth'
      })
    }
  }
}
</script>

<style lang='scss'>
  .footer {
    background-color: #223263;
    &__top {
      padding: 140px 0;
    }
    &__title {
      @include font(28px, 35px, #F4F5F7);
      margin-bottom: 57px;
    }
    &__links {
      display: flex;
      flex-direction: column
    }
    &__link,
    &__contact {
      @include font(18px, 46px, #EBF0FF);
      width: max-content;
    }

    &__brand-logo {
      margin-bottom: 28px;
      justify-content: space-between;
      &, > div {
        display: flex;
        align-items: center;
      }
      img {
        height: 72px;
        width: 43px;
        margin-right: 10px
      }
    }
    &__brand-name {
      @include font(35px, 40px, white, bold);
    }
    &__go-top {
      justify-self: flex-end;
      transition: background-color 300ms ease-in-out;
      border-radius: 2px;
      i {
        font-size: 32px;
        color: white;
        transition: color 300ms ease-in-out;
      }
      &:hover {
        background-color: white;
        i {
          color: #223263;
        }
      }
    }
    &__newsletter-title {
      @include font(23px, 23px, #F4F5F7, 600);
      margin-bottom: 36px;
    }
    &__newsletter-form {
      display: flex;
      .vs-input {
        height: 71px;
        width: 100%;
        border-radius: 8px 0;
        @include font(16px, 18px, #223263);
      }
    }
    &__newsletter-input {
      margin-right: 26px;
      flex: 1;
    }
    &__newsletter-button {
      height: 71px;
      width: 71px;
      background-color: #3B96D2;
      border-radius: 8px 0;
      i {
        font-size: 21px;
      }
    }
    &__divider {
      border: none;
      height: 2px;
      background-color: rgba(#EBF0FF, 0.1);
    }
    &__bottom {
      min-height: 71px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    &__copyright {
      @include font(18px, 46px, rgba(#EBF0FF, 0.8));
    }
    &__social-link {
      font-size: 18px;
      color: #EBF0FF;
      &:not(:last-child) {
        margin-right: 34px;
      }
    }
  }
</style>
