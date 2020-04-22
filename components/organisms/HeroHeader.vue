<template>
  <SfHero :style="{margin: 'auto' }">
    <!-- <SfHeroItem
      :title="title"
      :subtitle="subtitle"
      :button-text="buttonText"
      :image="image"
      :background="background" -->
    <!-- /> -->
    <SfHeroItem
      title="Colorful summer dresses are already in store"
      subtitle="Las nuevas colecciones"
      button-text="Ver todas"
      image="/images/hero/example.png"
      background="#FCE4EC"
    />
    <SfHeroItem
      title="Colorful summer dresses are already in store"
      subtitle="Las nuevas colecciones"
      button-text="Ver todas"
      image="/images/hero/example.png"
      background="#FCE4EC"
    />
  </SfHero>
</template>
<script>
import { SfHero } from "@storefront-ui/vue";

export default {
  name: 'HeroHeader',
  components: {
    SfHero
  },
};
</script>