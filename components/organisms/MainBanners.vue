<template>
  <SfBannerGrid
    :banner-grid="bannerGrid"
    :style="{ maxWidth: '1240px', margin: 'auto' }"
    class="--banner-grid-row-flex"
  >
    <template v-for="item in bannersExample" v-slot:[item.slot]>
      <SfBanner
        :key="item.slot"
        :title="item.title"
        :subtitle="item.subtitle"
        :description="item.description"
        :button-text="item.buttonText"
        :image="item.image"
        :class="item.class"
      />
    </template>
  </SfBannerGrid>
</template>
<script>
import { SfBannerGrid } from "@storefront-ui/vue";
import { SfBanner } from "@storefront-ui/vue";
export default {
  components: {
    SfBannerGrid,
    SfBanner
  },
  data() {
    return {
      bannersExample: [
        {
          slot: "banner-A",
          subtitle: ["Dresses"],
          title: ["Cocktail & Party"],
          description: [
            "Find stunning women's cocktail dresses and party dresses. Stand out in lace and metallic cocktail dresses from all your favorite brands."
          ],
          buttonText: ["Shop now"],
          image: ["/assets/storybook/Home/bannerF.jpg"],
          class: ["sf-banner--slim"]
        },
        {
          slot: "banner-B",
          subtitle: ["Dresses"],
          title: ["Linen Dresses"],
          description: [
            "Find stunning women's cocktail dresses and party dresses. Stand out in lace and metallic cocktail dresses from all your favorite brands.",
            ""
          ],
          buttonText: ["Shop now"],
          image: ["/assets/storybook/Home/bannerE.jpg"],
          class: ["sf-banner--slim"],
          // style: ["padding-right: 20%", null]
        },
      ]    };
  }
};
</script>