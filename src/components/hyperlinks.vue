<template>
  <div class="links-container">
    <hyperlink v-for="hyperlink in config.hyperlinks" v-bind:title="hyperlink.title" v-bind:href="hyperlink.href" v-bind:image="hyperlink.symbol" v-bind:key="hyperlink.title"></hyperlink>
  </div>
</template>

<script>
import hyperlink from "./hyperlink.vue"
import config from "../../config.json"

export default {
  name: "hyperlinks",

  data() {
    return {
      config: config
    }
  },

  components: {
    hyperlink,
  },
}
</script>

<style lang="scss">
.links-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 2.2vw;
}
</style>
