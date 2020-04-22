<template>
  <SfFooter :column="column" :multiple="multiple">
    <SfFooterColumn
      v-for="column in columns"
      :key="column.title"
      :title="column.title"
    >
      <SfList v-if="column.items">
        <SfListItem v-for="item in column.items" :key="item">
          <SfMenuItem :label="item" />
        </SfListItem>
      </SfList>
      <div v-else :style="{ display: 'flex', ...itemSpacer }">
        <SfImage
          v-for="picture in column.pictures"
          :key="picture"
          width="12"
          height="12"
          :src="'/assets/storybook/SfFooter/' + picture + '.svg'"
          :style="{ margin: '0 1.5rem 0 0' }"
        />
      </div>
    </SfFooterColumn>
  </SfFooter>
</template>
<script>
import { SfFooter } from "@storefront-ui/vue";
import { SfHeader } from "@storefront-ui/vue";
import { SfList } from "@storefront-ui/vue";
import { SfImage } from "@storefront-ui/vue";
import { SfButton } from "@storefront-ui/vue";
import { SfMenuItem } from "@storefront-ui/vue";
export default {
  components: {
    SfFooter,
    SfHeader,
    SfList,
    SfImage,
    SfButton,
    SfMenuItem
  },
  data() {
    return {
      isMobile: false,
      columns: [
        {
          title: "About us",
          items: ["Who we are", "Quality in the details", "Customer Reviews"]
        },
        {
          title: "Departments",
          items: ["Women fashion", "Men fashion", "Kidswear", "Home"]
        },
        {
          title: "Help",
          items: ["Customer service", "Size guide", "Contact us"]
        },
        { title: "Payment & delivery", items: ["Purchase terms", "Guarantee"] },
        {
          title: "Social",
          pictures: ["facebook", "pinterest", "twitter", "youtube"]
        }
      ],
      column: 4,
      multiple: false
    };
  }
};
</script>

<style lang="scss" scoped>
*{
  background-color:red;
  // color:white;
  // border-radius:8px;
}
</style>
