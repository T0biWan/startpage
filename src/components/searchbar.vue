<template>
  <section class="section">
    <form method="get" v-bind:action="this.search_engine_action">
      <div class="field has-addons">
        <div class="control has-icons-left">
          <span class="select">
              <select v-model="selected_search_engine">
                <option v-for="(value, key) in search_engines">{{key}}</option>
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
export default {
  name: "searchbar",

  data() {
    return {
      selected_search_engine: 'duckduckgo',

      search_engines: {
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
    search_engine_action: function() {
      return this.search_engines[this.selected_search_engine].action
    },
    search_engine_input_name: function() {
      return this.search_engines[this.selected_search_engine].name
    }
  }
}
</script>

<style lang="scss">
</style>
