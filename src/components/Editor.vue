<script setup lang="ts">
import { useSiteStore } from '~/stores/site'

const router = useRouter()
const siteStore = useSiteStore()
const options = siteStore.options
const pages = siteStore.pages
</script>

<template>
  <div w-90 p-6 relative h-screen shadow-lg>
    <div>
      <div>
        <div text-gray-500 uppercase>
          General
        </div>
        <div>
          <div my-4 />
          <div text-sm opacity-50>
            Logo
          </div>
          <div h-10 bg-gray-100 rounded-lg mt-1 cursor-pointer hover:bg-gray-200 />
        </div>
        <div>
          <div my-4 />
          <div text-sm opacity-50>
            Title
          </div>
          <input v-model="options.title.value" type="text">
        </div>
        <div>
          <div my-4 />
          <div text-sm opacity-50>
            Description
          </div>
          <input v-model="options.description.value" type="text">
        </div>
      </div>
      <div absolute bottom-0 w-full hidden>
        <div bg-blue-600 text-white px-4 py-2 rounded-lg w-full>
          save
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
input {
  @apply px-2 py-2 rounded border-gray-300 w-full border mt-1
}
</style>
