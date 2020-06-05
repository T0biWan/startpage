<template>
  <div id="app">
    <div class="container_row">
      <div class="background-gradient h-screen"></div>
      <div class="background-image"></div>
      <div class="foreground text-white">
        <div v-for="link in links" :key="link.title" class="bg-link">
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
        { title: 'youtube', link: 'https://www.youtube.com/', category: '', icon: '' },
        { title: 'udemy', link: 'https://www.udemy.com/home/my-courses/learning/', category: '', icon: '' },
        { title: 'imgur', link: 'https://imgur.com/t/meme%20dump', category: '', icon: '' },
        { title: 'picdumbs', link: 'https://www.picdumps.com/', category: '', icon: '' },
        { title: 'netflix', link: 'https://www.netflix.com/browse', category: '', icon: '' },
        { title: 'prime', link: 'https://www.amazon.de/Prime-Video/', category: '', icon: '' },
        { title: 'calender', link: 'https://calendar.google.com/calendar/r', category: '', icon: '' },
        { title: 'contacts', link: 'https://contacts.google.com/', category: '', icon: '' },
        { title: 'maps', link: 'https://www.google.com/maps/', category: '', icon: '' },
        { title: 'maps timeline', link: 'https://www.google.com/maps/timeline', category: '', icon: '' },
        { title: 'notes', link: 'https://github.com/T0biWan/notes-cms', category: '', icon: '' },
        { title: 'disroot', link: 'https://apps.disroot.org/', category: '', icon: '' },
        { title: 'tasks', link: 'https://trello.com/b/SKPdrjlw/task-force', category: '', icon: '' }
      ]
    }
  }
}
</script>

<style>
.bg-link {
  /* background-color: rgb(18, 4, 40); */
  /* background-image: linear-gradient(to right, rgb(143, 32, 98), rgb(9, 2, 53)); */
  /* background-color: white; */
}

.container_row{
  display: grid;
}

.background-image, .background-gradient, .foreground {
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
