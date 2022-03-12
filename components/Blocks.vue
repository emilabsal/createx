<template>
  <div class="blocks">
    <div class="block">
      <img class="block-img" src="../assets/image/blocks/block1.png" alt="" />
      <div class="block-subtitle">Summer Collections</div>
      <div class="block-title">Sale Up to 70%</div>
      <NuxtLink to="/" class="block-link">Explore new prices</NuxtLink>
    </div>
    <div class="block">
      <img class="block-img" src="../assets/image/blocks/block2.png" alt="" />
      <div class="block-subtitle">Deal of the week</div>
      <div class="block-title">Stay Warm With Our New Sweaters</div>
      <NuxtLink to="/" class="block-link">Shop Now</NuxtLink>
    </div>
    <div class="block">
      <img class="block-img" src="../assets/image/blocks/block3.png" alt="" />
      <div class="block-subtitle">Summer Collections</div>
      <div class="block-title">Sale Up to 70%</div>
      <NuxtLink to="/" class="block-link">Explore new prices</NuxtLink>
    </div>
    <div class="block">
      <img class="block-img" src="../assets/image/blocks/block4.png" alt="" />
      <div class="block-subtitle">Summer Collections</div>
      <div class="block-title">Sale Up to 70%</div>
      <NuxtLink to="/" class="block-link">Explore new prices</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '../assets/scss/utils/variables';

.blocks {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 500px 500px;
  gap: 16px;
  margin-bottom: 180px;
}

.block {
  position: relative;
  z-index: 1;
  padding: 60px;

  &-img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    object-fit: cover;
  }

  &-subtitle {
    font-size: 14px;
    line-height: 150%;
    font-weight: bold;
    text-transform: uppercase;
    margin-bottom: 12px;
    color: #1e212c;
    letter-spacing: 1px;
  }

  &-title {
    font-size: 32px;
    line-height: 130%;
    font-weight: 900;
    color: #1e212c;
    margin-bottom: 40px;
  }

  &-link {
    display: inline-block;
    padding: 0 32px;
    border: 1px solid #17696a;
    border-radius: 4px;
    font-size: 14px;
    line-height: 44px;
    color: #17696a;
    font-weight: bold;
    letter-spacing: 0.5px;
    transition: 0.5s ease;
    outline: none;

    &:hover,
    &:focus {
      color: $lightColor;
      background-color: #17696a;
    }
  }
}

.block:nth-child(2) {
  grid-column: span 2;
}

.block:nth-child(3) {
  grid-column: span 2;
}
</style>
