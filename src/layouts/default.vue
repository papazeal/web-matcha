<script setup lang="ts">
import * as data from '~/data/data.json'
import { useSiteStore } from '~/stores/site'

const router = useRouter()
const siteStore = useSiteStore()
const options = siteStore.options
const pages = siteStore.pages
console.log('test')
</script>

<template>
  <div flex>
    <Editor hidden lg:block />
    <main class="font-sans min-h-full p-6 sm:py-4 text-gray-800 flex flex-col flex-1 bg-white">
      <Header />
      <RouterView my-12 sm:my-12 grow max-w-md w-full mx-auto />
      <Footer />
    </main>
  </div>
</template>
