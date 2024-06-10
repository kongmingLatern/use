<script setup lang='ts'>
import Form from './Form.vue'

const forms = [
  {
    type: 'text',
    path: 'name',
    slots: {
      prefix: (formValue) => {
        return 'com12313'
      },
      suffix: 'suffix',
    },
  },
  {
    type: 'textarea',
    path: 'desc',
  },
] as any[]
</script>

<template>
  <Form :forms="forms" />
</template>

<style scoped>

</style>
