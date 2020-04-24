<template>
  <div>
      <banner/>
      <category-nav/>
      <side-bar/>
  </div>
</template>

<script>
import SideBar from '@/components/organisms/layout/SideBar';
import Banner from '@/components/molecules/Banner.vue';
import CategoryNav from '@/components/molecules/CategoryNav.vue';

export default {
    name: 'CategoriesPage',
    layout: 'shop',
    components: {
      CategoryNav,
      Banner,
      SideBar,
    },
};
</script>

<style lang="scss" scoped>

</style>
