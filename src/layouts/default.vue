<script setup lang="ts">
import * as data from '~/data/data.json'
const router = useRouter()

</script>

<template>
  <main class="font-sans min-h-full p-6 sm:py-4 text-gray-800 flex flex-col flex-1 bg-gray-100">
    <header flex>
      <div>
        <RouterLink to="/">
          <div flex>
            <img src="https://api.iconify.design/twemoji:bagel.svg?color=%23888888" mr-6 h-12>
            <div>
              <div text-2xl>
                Web Matcha
              </div>
              <div opacity-50 mt--1>
                website editor & deployer
              </div>
            </div>
          </div>
        </RouterLink>
      </div>
      <div ml-auto>
        <div hidden sm:flex mx--3>
          <RouterLink v-for="item in data.pages" :to="'/'+item.slug" mx-3 py-1 uppercase>
            {{ item.title }}
          </RouterLink>
        </div>
        <div sm:hidden>
          <RouterLink v-if="router.currentRoute.value.name != 'menu'" to="/menu">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="iconify iconify--ri" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24" w-6 cursor-pointer><path fill="currentColor" d="M3 4h18v2H3V4zm6 7h12v2H9v-2zm-6 7h18v2H3v-2z" /></svg>
          </RouterLink>
          <RouterLink v-else to="/">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="iconify iconify--ri" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24" h-8 mr--1 mt--1 cursor-pointer><path fill="currentColor" d="m12 10.586l4.95-4.95l1.414 1.414l-4.95 4.95l4.95 4.95l-1.414 1.414l-4.95-4.95l-4.95 4.95l-1.414-1.414l4.95-4.95l-4.95-4.95L7.05 5.636z" /></svg>
          </RouterLink>
        </div>
      </div>
    </header>
    <RouterView my-12 sm:my-12 grow max-w-md w-full mx-auto />
    <Footer />
  </main>
</template>
