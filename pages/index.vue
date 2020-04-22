<template>
  <div>
    <SfAccordion
      :open="open"
      :multiple="multiple"
      :show-chevron="showChevron"
      :transition="transition"
    >
      <SfAccordionItem
        v-for="accordion in accordions"
        :key="accordion.header"
        :header="accordion.header"
      >
        <SfList>
          <SfListItem v-for="item in accordion.items" :key="item.label">
            <SfMenuItem :label="item.label" :count="item.count" />
          </SfListItem>
        </SfList>
      </SfAccordionItem>
    </SfAccordion>
  </div>
</template>
<script>
import { SfAccordion, SfList, SfMenuItem } from '@storefront-ui/vue'

export default {
  components: {
    SfAccordion,
    SfList,
    SfMenuItem
  },
  data () {
    return {
      accordions: [
        {
          header: 'Clothing',
          items: [
            { label: 'All', count: '280' },
            { label: 'Skirts', count: '11' },
            { label: 'Dresses', count: '32' }
          ]
        },
        {
          header: 'Accessories',
          items: [
            { label: 'All', count: '80' },
            { label: 'Belts', count: '101' },
            { label: 'Bag', count: '2' }
          ]
        },
        {
          header: 'Shoes',
          items: [
            { label: 'All', count: '2' },
            { label: 'Trainers', count: '22' },
            { label: 'Sandals', count: '55' }
          ]
        }
      ],
      open: 'Clothing',
      multiple: false,
      showChevron: false,
      transition: 'fade'
    }
  }
}
</script>

<style lang="scss" scoped>
  div{
    display:flex;
    max-width:10vw;
  }
</style>
