<script setup lang='ts'>
defineProps({
  element: {
    type: [Function, String],
    default: () => ({}),
  },
})
</script>

<template>
  <component
    :is="element"
    v-if="typeof element === 'function'"
  />
  <slot v-else>
    <span>
      {{ element }}
    </span>
  </slot>
</template>

<style scoped>

</style>
