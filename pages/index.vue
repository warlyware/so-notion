<template>
  <div class="app-container bg-blue-300 px-12 pt-8 h-full">
    <div class="bg-white rounded-t-lg w-full max-w-5xl h-screen overflow-scroll shadow">
      <div class="flex flex-col self-center justify-center min-h-full">
        <logo class="block self-center mt-8" />
        <h1 class="text-6xl -mb-4">
          So Notion!
        </h1>
        <h2 class="text-lg font-thin uppercase tracking-widest pb-8">
          Weekly Newsletter
        </h2>
        <hr class="w-2/3 self-center">
        <p class="text-xl pb-8 max-w-md self-center text-center">
          Get Notion tips, featured community workspaces, office hours summaries, and more, delivered weekly to your inbox.
        </p>
        <form
          class="w-full self-center flex flex-col items-center bg-gray-100 py-4 rounded mb-8"
          action="https://tinyletter.com/so-notion"
          method="post"
          target="popupwindow"
          :onsubmit="submitEmail">
          <label
            class="mb-2 tracking-wide"
            for="tlemail">
            Enter your email address to subscribe:
          </label>
          <input
            id="tlemail"
            class="w-64 block border p-2 mb-4"
            type="text"
            name="email">
          <input type="hidden" value="1" name="embed">
          <input
            class="px-4 py-2 w-40 text-white rounded-lg bg-blue-400 uppercase block cursor-pointer"
            type="submit"
            value="Subscribe">
        </form>
        <div class="pb-16" />
      </div>
      <footer class="fixed bottom-0 left-0 insert-x-0 flex w-full justify-center py-1 bg-black text-white">
        Made with ❤︎ by &nbsp;
        <a href="//danward.dev" target="_blank">
          warlyware
        </a>.
      </footer>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  methods: {
    submitEmail() {
      window.open(
        'https://tinyletter.com/so-notion',
        'popupwindow',
        'scrollbars=yes,width=800,height=600'
      )
      return true
    }
  }
}
</script>

<style>
.app-container {
  @apply min-h-screen w-full flex justify-center items-center text-center mx-auto;
}
.shadow {
  box-shadow: 37px 9px 6px -12px rgba(80,128,144,0.82);
}

hr {
  height: 30px;
  border-style: solid;
  border-color: #8c8b8b;
  border-width: 1px 0 0 0;
  border-radius: 20px;
}
hr:before {
  display: block;
  content: "";
  height: 30px;
  margin-top: -31px;
  border-style: solid;
  border-color: #8c8b8b;
  border-width: 0 0 1px 0;
  border-radius: 20px;
}

</style>
