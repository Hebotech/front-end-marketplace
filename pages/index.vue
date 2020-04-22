<template>
  <div>
      <hero-header/>
      <MainBanners/>
      <feature-products/>
  </div>
</template>

<script>
import HeroHeader from '@/components/organisms/HeroHeader';
import MainBanners from '@/components/organisms/MainBanners';
import FeatureProducts from '@/components/organisms/FeatureProducts';

export default {
  components: {
    HeroHeader,
    FeatureProducts,
    MainBanners,
  },
}
</script>

<style lang="scss" scoped>
</style>
