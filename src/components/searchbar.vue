<template>
<section class="section">

  <!-- <template v-if="selected_search_engine == 'google'">
      <form method="get" action="http://www.google.com/search">
        <div class="field has-addons">
          <selectbox v-bind:search_engines="this.search_engines"></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." name="q" maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template> -->

  <!-- <template v-else-if="selected_search_engine == 'dict.cc'">
      <form method="get" action="https://dict.cc/">
        <div class="field has-addons">
          <selectbox v-bind:search_engines="this.search_engines"></selectbox>
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
          <selectbox v-bind:search_engines="this.search_engines"></selectbox>
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
          <selectbox v-bind:search_engines="this.search_engines"></selectbox>
          <div class="control is-expanded">
            <input class="input" type="text" placeholder="search..." name="q" maxlength="255">
          </div>
          <div class="control">
            <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
          </div>
        </div>
      </form>
    </template> -->

    <form method="get" v-bind:action="this.search_engine_action">
      <div class="field has-addons">
        <!-- <selectbox v-bind:search_engines="this.search_engines"></selectbox> -->
        <div class="control has-icons-left">
          <span class="select">
            <select v-model="selected_search_engine">
              <option v-for="search_engine in search_engines">{{search_engine}}</option>
            </select>
          </span>
          <span class="icon is-small is-left">
            <i class="fab fa-searchengin"></i>
          </span>
        </div>
        <div class="control is-expanded">
          <input class="input" type="text" placeholder="search..." v-bind:name="search_engine_input_name" maxlength="255">
        </div>
        <div class="control">
          <button type="submit" class="button is-info"><i class="fas fa-search"></i></button>
        </div>
      </div>
    </form>
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
        "dict",
        "dees",
        // "wikipedia.de",
        // "wikipedia.com",
        // "Metal Archive"
      ],

      search_engine_propertys: {
        google: {
          action: "http://www.google.com/search",
          name: "q"
        },
        duckduckgo: {
          action: "https://duckduckgo.com/",
          name: "q"
        },
        dict: {
          action: "https://dict.cc/",
          name: "s"
        },
        dees: {
          action: "https://dees.dict.cc/",
          name: "s"
        }
      },
    }
  },

  computed: {
    search_engine_action: function () {
      return this.search_engine_propertys[this.selected_search_engine].action
    },
    search_engine_input_name: function () {
      return this.search_engine_propertys[this.selected_search_engine].name
    }
  }
}
</script>

<style lang="scss">
</style>
