<template>
<div>
  <h1 class="text-center">
    Los Favoritos
  </h1>
  <SfCarousel :style="{ maxWidth: '1140px', margin: 'auto' }">
    <SfCarouselItem>
        <ProductCard/>
    </SfCarouselItem>
    <SfCarouselItem>
        <ProductCard/>
    </SfCarouselItem>
    <SfCarouselItem>
        <ProductCard/>
    </SfCarouselItem>
  </SfCarousel>
</div>
</template>
<script>
import { SfProductCard } from "@storefront-ui/vue";
import { SfCarousel } from "@storefront-ui/vue";
import ProductCard from '@/components/molecules/ProductCard';

export default {
  components: {
    SfCarousel,
    SfProductCard,
    ProductCard,
  }
};
</script>

<style lang="scss" scoped>
h1{
  font-family:ThirdRail;
}
</style>