<template>
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
</template>

<script>
export default {
  name: "selectbox",

  props: {
    search_engines: {
      type: Array
    }
  },

  data() {
    return {
      selected_search_engine: 'duckduckgo',
    }
  }

}
</script>

<style lang="scss"></style>
