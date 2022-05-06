<template>
  <main class="font-sans min-h-full px-4 py-10  text-gray-700 dark:text-gray-200 dark:bg-gray-900">
    <div max-w-sm mx-auto>
      <header mb-10 flex>
        <div>
          <div>
            <div text-xl>
              Web Matcha
            </div>
            <div opacity-50 mt--2px>
              website editor & deployer
            </div>
          </div>
        </div>
        <div ml-auto>
          <nuxt-link to="/menu">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="iconify iconify--ri" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24" h-6 cursor-pointer><path fill="currentColor" d="M3 4h18v2H3V4zm6 7h12v2H9v-2zm-6 7h18v2H3v-2z" /></svg>
          </nuxt-link>
        </div>
      </header>
      <RouterView />
      <Footer mt-12 />
    </div>
  </main>
</template>
