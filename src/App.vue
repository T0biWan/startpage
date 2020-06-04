<template>
  <div id="app">
    <div class="container_row">
      <div class="background-gradient h-screen"></div>
      <div class="background-image"></div>
      <div class="foreground text-white">
        <div v-for="link in links" :key="link.title">
          <a :href="link.link">{{ link.title }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',

  data () {
    return {
      links: [
        { title: 'youtube', link: 'https://www.youtube.com/', icon: '' },
        { title: 'udemy', link: 'https://www.udemy.com/home/my-courses/learning/', icon: '' },
        { title: 'imgur', link: 'https://imgur.com/t/meme%20dump', icon: '' },
        { title: 'picdumbs', link: 'https://www.picdumps.com/', icon: '' },
        { title: 'netflix', link: 'https://www.netflix.com/browse', icon: '' },
        { title: 'prime', link: 'https://www.amazon.de/Prime-Video/', icon: '' },
        { title: 'calender', link: 'https://calendar.google.com/calendar/r', icon: '' },
        { title: 'contacts', link: 'https://contacts.google.com/', icon: '' },
        { title: 'maps', link: 'https://www.google.com/maps/', icon: '' },
        { title: 'maps timeline', link: 'https://www.google.com/maps/timeline', icon: '' },
        { title: 'notes', link: 'https://github.com/T0biWan/notes-cms', icon: '' },
        { title: 'disroot', link: 'https://apps.disroot.org/', icon: '' }
      ]
    }
  }
}
</script>

<style>
.container_row{
  display: grid;
}

.background-image, .background-gradient, .foreground{
  grid-column: 1;
  grid-row: 1;
}

.background-gradient {
  /* background-image: linear-gradient(to left, rgb(67, 52, 132), rgb(22, 33, 50)); */

  /* background-image: linear-gradient(to left, rgb(192, 88, 139), rgb(8, 2, 40)); */

  background-image: linear-gradient(to left, rgb(211, 50, 104), rgb(38, 17, 58));
  z-index: -2
}

.background-image {
  background: url(./assets/background_1.jpg);
  height: 100%;
  opacity: 0.15;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  z-index: -1
}
</style>
