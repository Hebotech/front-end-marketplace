<template>
  <div>
    <navi/>
    <banner/>
    <category-nav/>
    <side-bar
      class="side-bar"
    />
    <nuxt
      class="main-content"
    />
    <v-footer/>
  </div>
</template>

<script>
import Navi from '@/components/organisms/layout/Nav.vue';
import vFooter from '@/components/organisms/layout/Footer.vue';

import SideBar from '@/components/organisms/layout/SideBar';
import Banner from '@/components/molecules/Banner.vue';
import CategoryNav from '@/components/molecules/CategoryNav.vue';

export default {
  components: {
    Navi,
    vFooter,
    CategoryNav,
    Banner,
    SideBar,
  },
};
</script>

<style lang='scss' scoped>
.side-bar{
  position: absolute;
}
.main-content{
  margin-left:15vw;
}
</style>
