<template>
  <section class="section">
    <!-- https://dees.dict.cc/?s=test -->
    <!-- https://dees.dict.cc/?s=test -->
    <!-- http://www.google.com/search -->
    <form method="get" action="http://www.google.com/search">
      <div class="field has-addons">
        <div class="control has-icons-left">
          <span class="select">
            <select v-model="selected_search_engine">
              <option>google</option>
              <option>duckduckgo</option>
              <option>dict.cc</option>
              <option>dees.cc</option>
              <option>google images</option>
              <option>wikipedia.de</option>
              <option>wikipedia.com</option>
              <option>Metal Archive</option>
            </select>
          </span>
          <span class="icon is-small is-left">
            <i class="fab fa-searchengin"></i>
          </span>
        </div>
        <div class="control is-expanded">
          <input class="input" type="text" placeholder="search..." name="query" maxlength="255">
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
}
</script>

<style lang="scss">
@import 'node_modules/sass-material-design-colors/palette.scss';
</style>
