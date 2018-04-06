<template>
<div id="app">
  <div class="container">
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
    <!-- <linkbox title="Google Calendar" href="https://calendar.google.com/calendar/r"></linkbox>
        <linkbox title="Google Contacts" href="https://contacts.google.com/"></linkbox> -->

    <div class="links-container">
      <div class="link">1</div>
      <div class="link">2</div>
      <div class="link">3</div>
      <div class="link">4</div>
      <div class="link">5</div>
      <div class="link">6</div>
      <div class="link">7</div>
      <div class="link">8</div>
    </div>

  </div>
</div>
</template>

<script>
import logo from "./components/logo.vue"
import linkbox from "./components/linkbox.vue"
import searchbar from "./components/searchbar.vue"

export default {
  name: 'app',

  components: {
    logo,
    linkbox,
    searchbar,
  },
}
</script>

<style lang="scss">
@import 'node_modules/sass-material-design-colors/palette.scss';

.links-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 2.2vw;
}

.link {
    color: #5995DA;
    background-color: $grey-400;
    width: 11vw;
    height: 11vw;
    margin-bottom: 2.2vw;
}

.container {
    width: 50%;
}
</style>
