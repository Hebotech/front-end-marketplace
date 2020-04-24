<template>
  <SfBreadcrumbs :breadcrumbs="breadcrumbs" />
</template>
<script>
import { SfBreadcrumbs } from "@storefront-ui/vue";
export default {
  components: {
    SfBreadcrumbs,
  },
  data() {
    return {
      breadcrumbs: [
        { text: "Home", route: { link: "#" } },
        { text: "Category", route: { link: "#" } },
        { text: "Pants", route: { link: "#" } },
      ],
    };
  },
};
</script>