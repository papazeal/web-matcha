<script setup lang="ts">
import * as data from '~/data/data.json'
console.log(data)
</script>

<template>
  <div>
    <div opacity-50 mb-4 hidden>
      Menu
    </div>
    <RouterLink v-for="item in data.pages" :to="item.slug" block py-1 text-lg pl-6 relative>
      <div w-2 h-2 rounded-full bg-gray-300 absolute left-1 top-13px />{{ item.title }}
    </RouterLink>
    <div my-10 />
    <div hidden>
      twitter
    </div>
  </div>
</template>
