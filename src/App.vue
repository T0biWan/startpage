<template>
  <div id="app">
    <logo></logo>
    <searchbar></searchbar>

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
import searchbar from "./components/searchbar.vue"

export default {
  name: 'app',

  components: {
    logo,
    hero,
    linkbox,
    searchbar
  },
}
</script>

<style lang="scss"></style>
