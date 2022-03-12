<template>
  <swiper class="swiper slider" :options="swiperOption">
    <swiper-slide class="swiper-slide">
      <div class="container">
        <div class="slider">slider</div>
      </div>
    </swiper-slide>
    <swiper-slide class="swiper-slide">Slide 2</swiper-slide>
    <swiper-slide class="swiper-slide">Slide 3</swiper-slide>
    <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div>
  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/swiper.min.css'
import 'swiper/swiper-bundle.css'

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  name: 'Slider',
  data() {
    return {
      swiperOption: {
        slidesPerView: 1,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
      },
    }
  },
}
</script>
