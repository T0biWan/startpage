<template>
<section class="section">

  <template v-if="selected_search_engine == 'google'">
      <form method="get" action="http://www.google.com/search">
        <div class="field has-addons">
          <selectbox v-bind:search_engines=this.search_engines></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." name="q" maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template>

  <template v-else-if="selected_search_engine == 'dict.cc'">
      <form method="get" action="https://dict.cc/">
        <div class="field has-addons">
          <selectbox v-bind:search_engines=this.search_engines></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." name="s" maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template>

  <template v-else-if="selected_search_engine == 'dees.cc'">
      <form method="get" action="https://dees.dict.cc/">
        <div class="field has-addons">
          <selectbox v-bind:search_engines=this.search_engines></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." name="s" maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template>

  <template v-else-if="selected_search_engine == 'duckduckgo'">
      <form method="get" action="https://duckduckgo.com/">
        <div class="field has-addons">
          <selectbox v-bind:search_engines=this.search_engines></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." name="q" maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template>

  <template v-else-if="selected_search_engine == 'wikipedia.de'">
      <form method="get" action="https://de.wikipedia.org/wiki/">
        <div class="field has-addons">
          <selectbox v-bind:search_engines=this.search_engines></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template>

</section>
</template>

<script>
import selectbox from "./selectbox.vue"

export default {
  name: "searchbar",

  components: {
    selectbox,
  },

  data() {
    return {
      selected_search_engine: 'google',
      search_engines: [
        "google",
        "duckduckgo",
        "dict.cc",
        "dees.cc",
        // "wikipedia.de",
        // "wikipedia.com",
        // "Metal Archive"
      ]
    }
  }
}
</script>

<style lang="scss">
@import 'node_modules/sass-material-design-colors/palette.scss';
</style>
