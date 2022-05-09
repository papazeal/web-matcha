<script setup lang="ts">
import { useSiteStore } from '~/stores/site'

const router = useRouter()
const siteStore = useSiteStore()
const options = siteStore.options
const pages = siteStore.pages
</script>

<template>
  <header flex>
    <div>
      <RouterLink to="/">
        <div flex mt-6 sm:mt-0>
          <img src="https://api.iconify.design/twemoji:bagel.svg?color=%23888888" mr-4 h-12>
          <div>
            <div text-2xl>
              {{ options.title.value }}
            </div>
            <div opacity-50 mt--5px>
              {{ options.description.value }}
            </div>
          </div>
        </div>
      </RouterLink>
    </div>
    <div ml-auto>
      <div hidden md:flex mx--3>
        <RouterLink v-for="item in pages" :to="'/'+item.slug" mx-3 py-1 uppercase>
          {{ item.title }}
        </RouterLink>
      </div>
      <div md:hidden>
        <RouterLink v-if="router.currentRoute.value.name != 'menu'" to="/menu">
          <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="iconify iconify--ri" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24" w-6 cursor-pointer><path fill="currentColor" d="M3 4h18v2H3V4zm6 7h12v2H9v-2zm-6 7h18v2H3v-2z" /></svg>
        </RouterLink>
        <RouterLink v-else to="/">
          <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="iconify iconify--ri" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24" h-8 mr--1 mt--1 cursor-pointer><path fill="currentColor" d="m12 10.586l4.95-4.95l1.414 1.414l-4.95 4.95l4.95 4.95l-1.414 1.414l-4.95-4.95l-4.95 4.95l-1.414-1.414l4.95-4.95l-4.95-4.95L7.05 5.636z" /></svg>
        </RouterLink>
      </div>
    </div>
  </header>
</template>
