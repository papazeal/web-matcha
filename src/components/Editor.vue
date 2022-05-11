<script setup lang="ts">
import { useSiteStore } from '~/stores/site'

const router = useRouter()
const siteStore = useSiteStore()
const options = siteStore.options
const pages = siteStore.pages
</script>

<template>
  <div w-90 relative z-10>
    <div flex flex-col h-screen fixed w-90 shadow-xl border-r border-gray-200 bg-gray-100>
      <div px-6 py-3 bg-white>
        General Settings
      </div>
      <div overflow-y-auto p-6 grow>
        <div>
          <div text-sm opacity-50>
            Logo
          </div>
          <div h-10 bg-white rounded-lg mt-1 cursor-pointer />
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
      <div px-6 py-4 bg-white shadow-xl z-10>
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
