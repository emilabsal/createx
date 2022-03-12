<template>
  <NuxtLink to="/" class="category">
    <img
      class="category-img"
      :src="`require(${category.img})`"
      alt="category.name"
    />
    <h2 class="category-name">{{ category.name }}</h2>
  </NuxtLink>
</template>

<script>
export default {
  props: ['category'],
}
</script>

<style lang="scss" scoped></style>
