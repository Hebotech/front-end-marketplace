<template>
  <div>
    <navi/>
    <nuxt />
    <v-footer/>
  </div>
</template>

<script>
import Navi from '@/components/organisms/layout/Nav.vue';
import vFooter from '@/components/organisms/layout/Footer.vue';

export default {
  components: {
    Navi,
    vFooter,
  },
};
</script>

<style>

</style>
