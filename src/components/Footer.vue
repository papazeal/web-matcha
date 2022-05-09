<script setup lang="ts">
// import { toggleDark } from '~/composables'

const { t, availableLocales, locale } = useI18n()

// const toggleLocales = () => {
//   // change to some real logic
//   const locales = availableLocales
//   locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
// }
</script>

<template>
  <div flex text-gray-400>
    <div>Build with <a href="#">Web Matcha</a></div>
    <div ml-auto>
      <div w-3 h-3 bg-green-500 rounded-full />
    </div>
  </div>
</template>
