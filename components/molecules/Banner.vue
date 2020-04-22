<template>
  <div>
    <SfBanner
      :class="customClass"
      :title="title"
      :subtitle="subtitle"
      :description="description"
      :button-text="buttonText"
      :image="image"
      :background="background"
    />
  </div>
</template>
<script>
import { SfBanner } from "@storefront-ui/vue";
export default {
  components: {
    SfBanner
  },
  data() {
    return {
      title: "Eco Sandals",
      subtitle: "Summer shoes",
      description:
        "The collection features formal and casual comfort shoes with a Danish design focus. Made from premium leathers and comfort.",
      buttonText: "Shop Now",
      image: {
        mobile: "/assets/storybook/SfBanner/Banner2.jpg",
        desktop: "/assets/storybook/SfBanner/Banner2.jpg"
      },
      background: "#e1e3e2"
    };
  }
};
</script>
