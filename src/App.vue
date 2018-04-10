<template>
<div id="app">
  <div class="container">
    <logo imagepath="src/assets/img/wave-logo-color.png"></logo>
    <searchbar></searchbar>
    <hyperlinks></hyperlinks>
  </div>
</div>
</template>

<script>
import logo from "./components/logo.vue"
import searchbar from "./components/searchbar.vue"
import hyperlinks from "./components/hyperlinks.vue"

export default {
  name: 'app',

  components: {
    logo,
    searchbar,
    hyperlinks,
  },
}
</script>

<style lang="scss">
.container {
    width: 50%;
}
</style>
