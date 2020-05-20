<template>
  <div class="flex flex-col justify-center">
    <logo class="block self-center mt-8" />
    <h1 class="font-family-niconne text-6xl -mb-4">
      So Notion!
    </h1>
    <h2 class="text-lg font-thin uppercase tracking-widest pb-8">
      Weekly Newsletter
    </h2>
    <hr class="w-2/3 self-center">
    <p class="text-xl pb-8 max-w-md self-center text-center px-4">
      Get Notion tips, featured community workspaces, office hours summaries, and more, delivered weekly to your inbox.
    </p>
    <form
      class="w-2/3 self-center flex flex-col items-center bg-gray-100 py-4 rounded mb-8"
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
