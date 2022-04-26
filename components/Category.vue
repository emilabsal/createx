<template>
  <NuxtLink to="/" class="category">
    <img class="category-img" :src="category.img" alt="" />
    <h2 class="category-name">{{ category.name }}</h2>
  </NuxtLink>
</template>

<script>
export default {
  props: ['category'],
  name: 'Category',
}
</script>

<style lang="scss" scoped>
.category {
  display: flex;
  flex-direction: column;
  align-items: center;

  &-name {
    font-size: 20px;
    line-height: 150%;
    font-weight: 700;
    color: #1e212c;
    margin-top: 24px;
  }
}
</style>
