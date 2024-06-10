<script setup lang='ts'>
import type { PropType } from 'vue'
import CustomRender from './CustomRender.vue'

defineProps({
  item: {
    type: Object as PropType<any>,
    default: () => ({}),
  },
})
</script>

<template>
  <n-input v-if="item.type === 'text'" placeholder="输入框">
    <template v-if="item.slots.prefix" #prefix>
      <CustomRender :element="item.slots.prefix" />
    </template>

    <template v-if="item.slots.suffix" #suffix>
      <CustomRender :element="item.slots.suffix" />
    </template>
  </n-input>

  <n-input v-else-if="item.type === 'textarea'" type="textarea" placeholder="文本域">
    <slot :name="item.path" />
  </n-input>
</template>

<style scoped>

</style>
