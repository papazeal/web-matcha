<script setup lang="ts">
import { useHead } from '@vueuse/head'

const props = defineProps<{ page: string }>()

useHead({
  title: props.page,
  meta: [
    {
      name: 'description',
      content: 'Website description',
    },
  ],
})
</script>

<template>
  <div max-w-sm mx-auto>
    <img src="../data/images/bb1.jpg">
    <div>page: {{ props.page }}</div>
    <div>content: {{ props.page }}</div>
  </div>
</template>
