<script setup lang="ts">
import * as data from '~/data/data.json'
console.log(data)
</script>

<template>
  <div>
    <div opacity-50 mb-4 hidden>
      Menu
    </div>
    <RouterLink v-for="item in data.pages" :to="item.slug" block py-1>
      {{ item.title }}
    </RouterLink>
  </div>
</template>
