<template>
  <form
    style="border:1px solid #ccc;padding:3px;text-align:center;"
    action="https://tinyletter.com/so-notion"
    method="post"
    target="popupwindow"
    onsubmit="window.open('https://tinyletter.com/so-notion', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true"
  >
    <p>
      <label for="tlemail">Enter your email address</label>
    </p>
    <p>
      <input id="tlemail" type="text" style="width:140px" name="email">
    </p>
    <input type="hidden" value="1" name="embed">
    <input type="submit" value="Subscribe">
    <p>
      <a href="https://tinyletter.com" target="_blank">powered by TinyLetter</a>
    </p>
  </form>
</template>

<script>

</script>

<style lang="scss" scoped>
</style>
