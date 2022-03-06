<template>
  <footer class="footer">
    <div class="footer-inner container">
      <div class="footer-col">
        <span class="footer-title">Help</span>
        <NuxtLink to="/" class="footer-link">Delivery & returns</NuxtLink>
        <NuxtLink to="/" class="footer-link">FAQ</NuxtLink>
        <NuxtLink to="/" class="footer-link">Track Order</NuxtLink>
        <NuxtLink to="/" class="footer-link">Contacts</NuxtLink>
        <NuxtLink to="/" class="footer-link">Blog</NuxtLink>
      </div>
      <div class="footer-col">
        <span class="footer-title">Shop</span>
        <NuxtLink to="/" class="footer-link">New arrivals</NuxtLink>
        <NuxtLink to="/" class="footer-link">Trending now</NuxtLink>
        <NuxtLink to="/" class="footer-link">Sales</NuxtLink>
        <NuxtLink to="/" class="footer-link">Brands</NuxtLink>
      </div>
      <div class="footer-col">
        <span class="footer-title">Get in touch</span>
        <p class="footer-contact">
          Call:
          <a href="tel:4055550128" class="footer-contact__link"
            >(405) 555-0128</a
          >
        </p>
        <p class="footer-contact">
          Email:
          <a href="mailto:hello@createx.com" class="footer-contact__link"
            >hello@createx.com</a
          >
        </p>
        <div class="footer-icons">
          <a href="/" class="footer-icon">
            <Icon name="facebook" :width="16" :height="16" fill="#ffffff" />
          </a>
          <a href="/" class="footer-icon">
            <Icon name="instagram" :width="16" :height="16" fill="#ffffff" />
          </a>
          <a href="/" class="footer-icon">
            <Icon name="twitter" :width="16" :height="16" fill="#ffffff" />
          </a>
          <a href="/" class="footer-icon">
            <Icon name="youtube" :width="16" :height="16" fill="#ffffff" />
          </a>
          <a href="/" class="footer-icon">
            <Icon name="pinterest" :width="16" :height="16" fill="#ffffff" />
          </a>
        </div>
      </div>
      <div class="footer-col">
        <span class="footer-title">Download our app</span>
        <div class="footer-mobile">
          <a href="/" class="footer-mobile__link">
            <img :src="store" alt="app store" />
          </a>
          <a href="/" class="footer-mobile__link">
            <img :src="play" alt="google play" />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import store from '../assets/image/app-store.svg'
import play from '../assets/image/google-play.svg'

export default {
  data: function () {
    return {
      store: store,
      play: play,
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/utils/basic.scss';

.footer {
  background-color: #1e212c;
  padding-top: 60px;
  padding-bottom: 74px;
  width: 100%;

  &-col:last-child {
    .footer-title {
      margin-bottom: 24px;
    }
  }

  &-inner {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 10px;
  }

  &-title {
    display: block;
    color: $lightColor;
    font-size: 16px;
    line-height: 160%;
    font-weight: bold;
    text-transform: uppercase;
    margin-bottom: 12px;
  }
  &-link {
    display: block;
    @include text;
    color: #ffffff99;
    margin-bottom: 4px;
  }

  &-contact {
    color: $lightColor;
    @include text;

    &:first-child {
      margin-bottom: 4px;
    }

    &__link {
      color: #ffffff99;
    }
  }

  &-icons {
    margin-top: 24px;
    display: flex;
  }

  &-icon {
    width: 32px;
    height: 32px;
    border-radius: 4px;
    background-color: rgba(255, 255, 255, 0.12);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 12px;

    &:hover {
      background-color: darken(rgba(255, 255, 255, 0.12), 40%);
    }
  }

  &-mobile {
    display: flex;

    &__link:first-child {
      margin-right: 20px;
    }
  }
}
</style>
