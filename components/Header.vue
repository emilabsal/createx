<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top__inner container">
        <p class="header-top__text">
          Available 24/7 at
          <a href="tel:84055550128" class="header-top__link">(405) 555-0128</a>
        </p>
        <nav class="nav-top">
          <ul class="nav-top__list">
            <li class="nav-top__item">
              <NuxtLink to="/" class="nav-top__link"
                >Delivery & returns</NuxtLink
              >
              <NuxtLink to="/" class="nav-top__link">Track order</NuxtLink>
              <NuxtLink to="/" class="nav-top__link">Blog</NuxtLink>
              <NuxtLink to="/" class="nav-top__link">Contacts</NuxtLink>
            </li>
          </ul>
        </nav>
        <div class="language">
          <div class="language__select">
            <div class="language__option">
              <img :src="flagam" alt="" />Eng / $
            </div>
          </div>
          <button class="language__toggle">
            <Icon name="arrow" :width="16" :height="16" fill="#ffffff99" />
          </button>
        </div>
        <select class="language-select" style="display: none">
          <option value="Eng" class="language-option"></option>
        </select>
        <button class="auth">
          <Icon name="profile" :width="16" :height="16" fill="#ffffff99" />
          Log in / Register
        </button>
      </div>
    </div>
    <div class="header-main">
      <div class="header-main__inner container">
        <div class="header-main__left">
          <NuxtLink to="/" class="logo">
            <img :src="logo" alt="" />
          </NuxtLink>
          <nav class="nav-main">
            <ul class="nav-main__list">
              <li class="nav-main__item">
                <NuxtLink to="/" class="nav-main__link">Women</NuxtLink>
                <NuxtLink to="/" class="nav-main__link">Men</NuxtLink>
                <NuxtLink to="/" class="nav-main__link">Girls</NuxtLink>
                <NuxtLink to="/" class="nav-main__link">Boys</NuxtLink>
                <NuxtLink to="/" class="nav-main__link nav-main__link_accent"
                  >Sale</NuxtLink
                >
              </li>
            </ul>
          </nav>
        </div>
        <div class="header-main__right">
          <div class="search">
            <input
              type="text"
              class="search-input"
              placeholder="Search for products..."
            />
            <button class="search-button">
              <Icon name="search" :width="16" :height="16" fill="#424551" />
            </button>
          </div>
          <div class="links">
            <div class="links-favor">
              <button class="links-favor__button">
                <Icon name="favor" :width="20" :height="20" fill="#424551" />
              </button>
              <span class="links-favor__num">2</span>
            </div>
            <div class="links-cart">
              <button class="links-cart__button" @click="countHandleCart">
                <Icon name="cart" :width="20" :height="20" fill="#424551" />
              </button>
              <span class="links-cart__num">{{ countCart }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="header-sale">
      <div class="header-sale__inner container">
        <Icon name="arrow" :width="16" :height="16" fill="#ffffff" />
        <p class="header-sale__text">
          Up to 70% Off.
          <a href="#" class="header-sale__link">Shop our latest sale styles</a>
        </p>
        <Icon name="arrow" :width="16" :height="16" fill="#ffffff" />
      </div>
    </div>
  </header>
</template>

<script>
import Icon from './Icon.vue'
import '../assets/scss/header.scss'
import flagam from '../assets/icon/flag-usa.svg'
import logo from '../assets/image/logo.svg'

export default {
  data: function () {
    return {
      flagam: flagam,
      logo: logo,
      countCart: 0,
    }
  },
  methods: {
    countHandleCart() {
      return (this.countCart += 1)
    },
  },
  components: {
    Icon,
  },
}
</script>
