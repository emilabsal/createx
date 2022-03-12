<template>
  <main class="main">
    <Slider />
    <nav class="nav-cat container">
      <ul class="nav-cat__list">
        <li class="nav-cat__item">
          <NuxtLink to="/" class="nav-cat__link">
            <img :src="women" alt="women category" />
            <span class="nav-cat__text">Women's</span>
          </NuxtLink>
        </li>
        <li class="nav-cat__item">
          <NuxtLink to="/" class="nav-cat__link">
            <img :src="men" alt="men category" />
            <span class="nav-cat__text">Men's</span>
          </NuxtLink>
        </li>
        <li class="nav-cat__item">
          <NuxtLink to="/" class="nav-cat__link">
            <img :src="kids" alt="kids category" />
            <span class="nav-cat__text">Kids</span>
          </NuxtLink>
        </li>
      </ul>
    </nav>
    <div class="arrivals-wrap">
      <h2 class="arrivals-wrap__title">New arrivals</h2>
      <p class="arrivals-wrap__text">
        Check out our latest arrivals for the upcoming season
        <br />
        <NuxtLink to="/" class="arrivals-wrap__link"
          >See the collection here</NuxtLink
        >
      </p>

      <Arrivals />
    </div>
    <Blocks />
  </main>
</template>

<script>
import Slider from '../components/Slider.vue'
import Arrivals from '../components/Arrivals.vue'
import women from '../assets/image/women.png'
import men from '../assets/image/men.png'
import kids from '../assets/image/kids.png'

export default {
  components: { Slider, Arrivals },
  name: 'IndexPage',
  data() {
    return {
      women: women,
      men: men,
      kids: kids,
    }
  },
}
</script>
