<template>
  <swiper class="swiper arrivals" :options="swiperOption">
    <swiper-slide class="swiper-slide" :key="card.id" v-for="card in cards"
      ><Card :product="card" />
    </swiper-slide>
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
  name: 'Arrivals',
  data() {
    return {
      swiperOption: {
        spaceBetween: 30,
        slidesPerView: 'auto',
      },
      cards: [
        {
          id: 1,
          img: require('@/assets/image/products/hat.png'),
          desc: 'Black and white sport cap',
          price: '18.15',
        },
        {
          id: 2,
          img: require('@/assets/image/products/glasses.png'),
          desc: 'Metal bridge sunglasses',
          price: '89.95',
        },
        {
          id: 3,
          img: require('@/assets/image/products/romper.png'),
          desc: 'Green baby romper',
          price: '20.40',
        },
        {
          id: 4,
          img: require('@/assets/image/products/jeans.png'),
          desc: 'Mid-rise slim cropped fit jeans',
          price: '40.00',
        },
        {
          id: 5,
          img: require('@/assets/image/products/earrings.png'),
          desc: 'Red dangle earrings',
          price: '29.95',
        },
        {
          id: 6,
          img: require('@/assets/image/products/shoes.png'),
          desc: 'Baby shoes with laces',
          price: '30.60',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.arrivals {
  margin-bottom: 180px;
}
</style>
