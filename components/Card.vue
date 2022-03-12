<template>
  <NuxtLink to="/" class="card">
    <Icon name="star" width="14" height="14" fill="#F89828" />
    <img :src="product.img" alt="" />
    <p class="card__description">{{ product.desc }}</p>
    <span class="card__price">${{ product.price }}</span>
  </NuxtLink>
</template>

<script>
export default {
  props: ['product'],
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/utils/variables';

.card {
  position: relative;
  width: 285px;
  display: inline-block;

  img {
    height: 320px;
    max-width: 100%;
    object-fit: cover;
  }

  svg {
    position: absolute;
    top: 16px;
    right: 1px;
  }

  &__description {
    font-size: 18px;
    line-height: 150%;
    margin-top: 16px;
    margin-bottom: 8px;
    color: $darkColor;
  }

  &__price {
    color: #1e212c;
    font-size: 20px;
    line-height: 130%;
    font-weight: bold;
  }
}
</style>
