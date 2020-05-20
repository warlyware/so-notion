<template>
  <div class="app-container bg-blue-300 px-12 pt-8 h-full">
    <div class="bg-white rounded-t-lg w-full max-w-5xl h-screen shadow px-4 flex justify-center items-center">
      <div class="max-h-full w-full m-auto overflow-auto">
        <nuxt />
      </div>
    </div>
    <footer class="fixed bottom-0 left-0 insert-x-0 flex w-full justify-center py-1 bg-black text-white">
      Made with ❤︎ by &nbsp;
      <a href="//danward.dev" target="_blank">
        warlyware
      </a>.
    </footer>
  </div>
</template>

<style>

.app-container {
  @apply min-h-screen w-full flex justify-center items-center text-center mx-auto;
}
.shadow {
  box-shadow: 37px 9px 6px -12px rgba(80,128,144,0.82);
}
</style>
