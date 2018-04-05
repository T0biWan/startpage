<template>
  <div id="app">
    <logo imagepath="src\assets\logo\wave-logo-color.png"></logo>
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
        <!-- <linkbox title="Google Calendar" href="https://calendar.google.com/calendar/r"></linkbox>
        <linkbox title="Google Contacts" href="https://contacts.google.com/"></linkbox> -->
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <div class="tile is-child">
              <article class="card">
                <p>
                  hallo
                </p>
              </article>
            </div>
          </div>
          <div class="tile is-parent">
            <div class="tile is-child">
              <article class="card">
                <p>
                  hallo
                </p>
              </article>
            </div>
          </div>
          <div class="tile is-parent">
            <div class="tile is-child">
              <article class="card">
                <p>
                  hallo
                </p>
              </article>
            </div>
          </div>
          <div class="tile is-parent">
            <div class="tile is-child">
              <article class="card">
                <p>
                  hallo
                </p>
              </article>
            </div>
          </div>

        </div>

        <!-- <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">One</p>
              <p class="subtitle">Subtitle</p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">Two</p>
              <p class="subtitle">Subtitle</p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">Three</p>
              <p class="subtitle">Subtitle</p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">Four</p>
              <p class="subtitle">Subtitle</p>
            </article>
          </div>
        </div> -->

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
    searchbar,
  },
}
</script>

<style lang="scss">
.abc {
  background: blue;
}

.container {
  width: 60%;
}
</style>
