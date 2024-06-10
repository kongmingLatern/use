<script setup lang='ts'>
import type { PropType } from 'vue'
import SimpleFormItem from './SimpleFormItem.vue'

defineProps({
  forms: {
    type: Array as PropType<any[]>,
    default: () => ([]),
  },
})
</script>

<template>
  <NForm>
    <SimpleFormItem
      v-for="(item, index) in forms"
      :key="index"
      :item="item"
    />
  </NForm>
</template>

<style scoped>

</style>
