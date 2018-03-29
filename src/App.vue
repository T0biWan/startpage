<template>
<div id="app">
  <hero title="In Production:">Selected search engine: {{selected_search_engine}}</hero>
  <logo></logo>

  <section class="section">
    <div class="field has-addons">
      <div class="control has-icons-left">
        <span class="select">
          <select v-model="selected_search_engine">
            <option>google</option>
            <option>duckduckgo</option>
            <option>dict.cc</option>
            <option>google images</option>
            <option>Wikipedia.de</option>
            <option>Wikipedia.com</option>
            <option>Metal Archive</option>
          </select>
        </span>
        <span class="icon is-small is-left">
          <i class="fab fa-searchengin"></i>
        </span>
      </div>
      <div class="control is-expanded">
        <input class="input" type="text" placeholder="Find a repository">
      </div>
      <div class="control">
        <a class="button is-info"><i class="fas fa-search"></i></a>
      </div>
    </div>
  </section>
</div>
</template>

<script>
  import logo from "./components/logo.vue"
  import hero from "./components/hero.vue"

  export default {
    name: 'app',

    components: {
      logo,
      hero
    },

    data() {
      return {selected_search_engine: 'google'}
    }
  }
</script>

<style lang="scss">
.logo-container {
  width: 250px
}
</style>
