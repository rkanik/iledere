<template>
  <header class="header">
    <div class="container">
      <div class="header__flex">
        <div class="header__left">
          <NuxtLink to="/" class="header__brand-logo">
            <img src="../assets/images/logo.png" alt="Brand Logo">
            <div class="header__brand-name">
              île de ré
            </div>
          </NuxtLink>
          <nav class="header__nav">
            <NuxtLink
              v-for="(nav, navIndex) in navs"
              :key="navIndex"
              :to="nav.path"
              class="header__nav-link"
            >
              {{ nav.name }}
            </NuxtLink>
          </nav>
        </div>
        <div class="header__actions">
          <div class="header__search">
            <i class="bx bx-search" />
          </div>
          <div class="header__lang">
            <i class="bx bx-globe" />
            <span>Fr</span>
          </div>
          <NuxtLink to="#" class="header__establish">
            Ajouter établissement
          </NuxtLink>
          <vs-button size="large" class="c-button header__register">
            S'inscrire
          </vs-button>
          <vs-button type="border" size="large" class="c-button header__login">
            Se connecter
          </vs-button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      navs: [
        { name: 'Bon Plan', path: '/bon-plan' },
        { name: 'Explorer L\'ile', path: '/explore' },
        { name: 'Se Loger', path: '/se-loger' },
        { name: 'Que faire sur l\'ile', path: '/que-faire-sur' },
        { name: 'Savoure', path: '/savoure' },
        { name: 'Vie Quotidienne', path: '/vie-quotidienne' }
      ]
    }
  }
}
</script>

<style lang='scss'>
  .header {
    z-index: 10;
    padding: 6px 0;
    position: relative;
    box-shadow: 0 6px 12px rgba(#3454D1, 0.14);
    &__flex, &__left {
      display: flex;
      align-items: center;
    }
    &__flex {
      justify-content: space-between;
    }
    &__brand-logo {
      display: flex;
      align-items: center;
      margin-right: 50px;
      img {
        margin-right: 20px
      }
    }

    &__brand-name {
      @include font(35px, 40px, #223263, bold);
    }

    &__nav-link {
      color: var(--text-primary);
      transition: opacity 300ms ease-in-out;
      &:not(:last-child) {
        margin-right: 36px;
      }
      &:hover {
        opacity: 0.5;
      }
    }

    &__actions {
      display: flex;
      align-items: center;
      & > *:not(:last-child) {
        margin-right: 16px;
      }
      i {
        font-size: 20px;
        color: #223263;
      }
    }
    &__lang,
    &__search {
      display: flex;
      align-items: center;
    }
    &__lang {
      @include font(20px, 34px, #223263, 500);
      i {
        margin-right: 4px;
      }
    }
    &__establish {
      @include font(16px, 18px, #3B96D2)
    }
    &__register.vs-button-primary {
      background-color: #3B96D2 !important;
    }
    &__login.vs-button-primary {
      color: #3B96D2 !important;
      border-color: #3B96D2 !important;
    }

  }
</style>
