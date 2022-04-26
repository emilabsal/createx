<template>
  <div class="categories container">
    <h2 class="categories-title">Popular categories</h2>
    <div class="categories-inner">
      <Category
        v-for="category in categories"
        :key="category.id"
        :category="category"
      />
    </div>
  </div>
</template>

<script>
import Category from './Category.vue'
export default {
  components: { Category },
  data() {
    return {
      categories: [
        {
          id: 1,
          img: require('@/assets/image/categories/tops.png'),
          name: 'Tops',
        },
        {
          id: 2,
          img: require('@/assets/image/categories/tshirts.png'),
          name: 'T-shirts',
        },
        {
          id: 3,
          img: require('@/assets/image/categories/caps.png'),
          name: 'Caps',
        },
        {
          id: 4,
          img: require('@/assets/image/categories/sandals.png'),
          name: 'Sandals',
        },
        {
          id: 5,
          img: require('@/assets/image/categories/jackets.png'),
          name: 'Jackets',
        },
        {
          id: 6,
          img: require('@/assets/image/categories/coats.png'),
          name: 'Coats',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.categories {
  margin-bottom: 180px;

  &-title {
    text-align: center;
    margin-bottom: 60px;
    font-size: 46px;
    line-height: 130%;
    font-weight: 900;
  }

  &-inner {
    display: flex;
    justify-content: space-between;
  }
}
</style>
