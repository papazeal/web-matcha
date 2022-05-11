<script setup lang="ts">
import { useHead } from '@vueuse/head'
import { useSiteStore } from '~/stores/site'
const siteStore = useSiteStore()
const options = siteStore.options
const pages = siteStore.pages
const props = defineProps<{ all: array }>()
const pageData = computed(() => {
  const slug = props.all[0] || ''
  return pages.filter(page => page.slug == slug)[0]
})

useHead({
  title: 'title',
  meta: [
    {
      name: 'description',
      content: '',
    },
  ],
})
</script>

<template>
  <div>
    <div hidden>
      <div>page: {{ props.all }}</div>
      <div>content: {{ props.all }}</div>
      {{ pageData }}
    </div>

    <div class="rtf">
      <div text-2xl mb-4>
        {{ pageData.title }}
      </div>
      <p>Muffin fruitcake toffee shortbread cake danish. Biscuit biscuit donut toffee candy chocolate bar croissant tart. Halvah sesame snaps powder soufflé soufflé tart wafer. Topping croissant pastry icing dessert sesame snaps brownie tart bonbon.</p>
      <img src="https://images.pexels.com/photos/1775043/pexels-photo-1775043.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" rounded my-10>
      <p>Muffin fruitcake toffee shortbread cake danish. Biscuit biscuit donut toffee candy chocolate bar croissant tart. Halvah sesame snaps powder soufflé soufflé tart wafer. Topping croissant pastry icing dessert sesame snaps brownie tart bonbon.</p>
      <p>Biscuit biscuit donut toffee candy chocolate bar croissant tart. Halvah sesame snaps powder soufflé soufflé tart wafer. Topping croissant pastry icing dessert sesame snaps brownie tart bonbon.</p>
      <div my-20 />
      <div>
        <img src="https://cdn-icons-png.flaticon.com/512/4193/4193312.png" w-60>
        <h3>Feature Rich</h3>
        <p>Muffin fruitcake toffee shortbread cake danish. Biscuit biscuit donut toffee candy chocolate bar croissant tart. Halvah sesame snaps powder soufflé soufflé tart wafer.</p>
        <p>
          <a href="#" bg-red text-white px-2 py-2 rounded-lg>Learn More ...</a>
        </p>
      </div>
      <div my-30 />
      <div>
        <img src="https://cdn-icons-png.flaticon.com/512/4193/4193320.png" w-60 inline-block>
        <h3>Support Center</h3>
        <p>Muffin fruitcake toffee shortbread cake danish. Biscuit biscuit donut toffee candy chocolate bar croissant tart. Halvah sesame snaps powder soufflé soufflé tart wafer.</p>
        <p>
          <a href="#" bg-red text-white px-2 py-2 rounded-lg>Learn More ...</a>
        </p>
      </div>
    </div>
  </div>
</template>
