<template>
<div id="app">
  <!-- <hero title="In Production:">Selected search engine: {{selected_search_engine}}</hero> -->
  <logo></logo>

  <section class="section">
    <form method="get" action="http://www.google.com/search">
      <div class="field has-addons">
        <div class="control has-icons-left">
          <span class="select">
            <select v-model="selected_search_engine">
              <option>google</option>
              <option>duckduckgo</option>
              <option>dict.cc</option>
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

  <!-- besser grid css oder flexbox ansehen und erst mal auf papier designen -->
  <!-- <section class="section">
    <div class="container">
      <div class="columns">
        <div class="column">
          <figure class="image is-128x128">
            <img src="https://bulma.io/images/placeholders/128x128.png">
          </figure>
        </div>
        <div class="column">
          <figure class="image is-128x128">
            <img src="https://bulma.io/images/placeholders/128x128.png">
          </figure>
        </div>
        <div class="column">
          <figure class="image is-128x128">
            <img src="https://bulma.io/images/placeholders/128x128.png">
          </figure>
        </div>
        <div class="column">
          <figure class="image is-128x128">
            <img src="https://bulma.io/images/placeholders/128x128.png">
          </figure>
        </div>
      </div>
    </div>
  </section> -->
  <section class="section">
    <div class="container">
      <linkbox title="Google Calendar" href="https://calendar.google.com/calendar/r"></linkbox>


    </div>

  </section>
</div>
</template>

<script>
import logo from "./components/logo.vue"
import hero from "./components/hero.vue"
import linkbox from "./components/linkbox.vue"

export default {
  name: 'app',

  components: {
    logo,
    hero,
    linkbox
  },

  data() {
    return {
      selected_search_engine: 'google'
    }
  }
}
</script>

<style lang="scss"></style>
