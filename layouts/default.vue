<template>
  <div>
    <navi/>
    <nuxt
      class="main-content"
    />
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
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

@font-face {
    font-family: 'ThirdRail';
    src: url('/fonts/third_rail_-_demo-webfont.woff2') format('woff2'),
         url('/fonts/third_rail_-_demo-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
.main-content{
  margin-top:8vw;
}
</style>
