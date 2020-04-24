<template>
  <div class="container">
      <div class="row m-0 justify-content-center breadcrumb">
        <breadcrumb/>
      </div>
      <div class="row m-0 ">
          <SfIcon :icon="'filter'" :size="'xxs'" :color="'primary-green'" :view-box="'viewBox'" />
          Fíltros
      </div>
  </div>
</template>

<script>
import { SfIcon } from "@storefront-ui/vue";
import Breadcrumb from '@/components/molecules/Breadcrumb.vue';

export default {
    name: 'CategoriesPage',
    layout: 'shop',
    components: {
      Breadcrumb,
      SfIcon
    },
};
</script>

<style lang="scss" scoped>

</style>