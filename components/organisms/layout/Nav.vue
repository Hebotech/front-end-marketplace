<template>
  <div>
    <SfHeader
      :title="title"
      :logo="'/images/basic/logo.png'"
      :active-icon="activeIcon"
      :has-mobile-search="hasMobileSearch"
      :search-placeholder="searchPlaceholder"
      :cart-icon="cartIcon"
      :wishlist-icon="wishlistIcon"
      :is-sticky="isSticky"
      :account-icon="accountIcon"
      :cart-items-qty="cartItemsQty"
      @click:cart="alert('@click:cart')"
      @click:wishlist="alert('@click:wishlist')"
      @click:account="alert('@click:account')"
    >
      <template #navigation>
        <SfHeaderNavigationItem v-for="item in navigation" :key="item">
          <nuxt-link
            to="/"
            :style="{
              display: 'flex',
              alignItems: 'center',
              justifyContent: 'space-around',
              height: '100%'
            }"
          >
            {{ item }}
          </nuxt-link>
        </SfHeaderNavigationItem>
      </template>
    </SfHeader>
    <StoriesPlaceholder #placeHolder :mobile="isMobile" />
  </div>
</template>

<script>
import { SfHeader } from "@storefront-ui/vue";
import { StoriesPlaceholder } from "@storefront-ui/vue";

export default {
  name: "Nav",
  components: {
    SfHeader,
    StoriesPlaceholder
  },
  data() {
    return {
      isMobile: true,
      navigation: ["Categorías", "Cosas", "Etcétera"],
      title: "Hebotech De México",
      logo: {
        mobile: { url: "../../public/basic/images/logo.png" },
        desktop: { url: "../../public/basic/images/logo.png" }
      },
      activeIcon: "account",
      hasMobileSearch: false,
      isSticky: true,
      searchPlaceholder: "Search for items",
      cartIcon: "empty_cart",
      wishlistIcon: "heart",
      accountIcon: "profile",
      cartItemsQty: "0"
    };
  }
};
</script>
