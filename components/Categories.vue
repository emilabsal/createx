<template>
  <Category
    v-for="category in categories"
    :key="category.id"
    :category="category"
  />
</template>

<script>
import Category from './Category.vue'
export default {
  components: { Category },
  data() {
    categories: [
      { id: 1, img: '@/assets/image/categories/tops.png', name: 'Tops' },
      { id: 2, img: '@/assets/image/categories/tshirts.png', name: 'T-shirts' },
      { id: 3, img: '@/assets/image/categories/caps.png', name: 'Caps' },
      { id: 4, img: '@/assets/image/categories/sandals.png', name: 'Sandals' },
      { id: 5, img: '@/assets/image/categories/jackets.png', name: 'Jackets' },
      { id: 6, img: '@/assets/image/categories/coats.png', name: 'Coats' },
    ]
  },
}
</script>

<style></style>
