<template>
  <div id="app">
    <div class="container_row">
      <div class="background-gradient h-screen"></div>
      <div class="background-image"></div>
      <div class="foreground text-white">
        <div class="mt-48 flex justify-center mx-32">
          <div class="flex flex-wrap">
            <div v-for="category in categorys()" :key="category" class="w-56 mx-4 mb-6">
              <h1 class="bg-category text-xl font-semibold pl-2 pb-2 pt-1">{{ category }}</h1>
              <div v-for="link in linksByCategory(category)" :key="link.title" class="bg-link pl-2 pb-2 text-lg"><a :href="link.link">{{ link.title }}</a></div>
            </div>
          </div>
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
        { title: 'tasks', link: 'https://trello.com/b/SKPdrjlw/task-force', category: 'office', icon: '' },
        { title: 'notes', link: 'https://github.com/T0biWan/notes-cms', category: 'office', icon: '' },
        { title: 'calender', link: 'https://calendar.google.com/calendar/r', category: 'office', icon: '' },
        { title: 'contacts', link: 'https://contacts.google.com/', category: 'office', icon: '' },
        { title: 'disroot', link: 'https://apps.disroot.org/', category: 'office', icon: '' },
        { title: 'master', link: 'https://github.com/T0biWan/notes-cms/blob/master/notes/studium/master-medieninformatik/13-WS20_masterarbeit/notes/masterarbeit.md', category: 'education', icon: '' },
        { title: 'udemy', link: 'https://www.udemy.com/home/my-courses/learning/', category: 'education', icon: '' },
        { title: '$lernen', link: 'https://trello.com/b/3G1kdMWc/lernen', category: 'education', icon: '' },
        { title: 'maps', link: 'https://www.google.com/maps/', category: 'services', icon: '' },
        { title: 'maps timeline', link: 'https://www.google.com/maps/timeline', category: 'services', icon: '' },
        { title: 'windfinder', link: 'https://de.windfinder.com/weatherforecast/tempelhof', category: 'services', icon: '' },
        { title: 'wetter', link: 'https://www.google.com/search?client=firefox-b-d&q=wetter+berlin', category: 'services', icon: '' },
        { title: 'fotos', link: 'https://photos.google.com/', category: 'services', icon: '' },
        { title: 'windy', link: 'https://www.windy.com/de/-Wetterradar-radar?radar,46.916,16.270,11', category: 'services', icon: '' },
        { title: 'youtube', link: 'https://www.youtube.com/', category: 'entertainment', icon: '' },
        { title: 'netflix', link: 'https://www.netflix.com/browse', category: 'entertainment', icon: '' },
        { title: 'prime', link: 'https://www.amazon.de/gp/video/storefront/', category: 'entertainment', icon: '' },
        { title: 'ard mediathek', link: 'https://www.ardmediathek.de/ard/', category: 'entertainment', icon: '' },
        { title: 'arte mediathek', link: 'https://www.arte.tv/de/', category: 'entertainment', icon: '' },
        { title: 'imgur', link: 'https://imgur.com/t/meme%20dump', category: 'entertainment', icon: '' },
        { title: 'picdumbs', link: 'https://www.picdumps.com/', category: 'entertainment', icon: '' }
      ]
    }
  },

  methods: {
    categorys () { return [...new Set(this.links.map(link => link.category))] },
    linksByCategory (category) { return this.links.filter(link => link.category === category) }
  }
}
</script>

<style>
.bg-category {
  background-color: rgba(255, 255, 255, 0.18);
}

.bg-link {
  background-color: rgba(255, 255, 255, 0.05);
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
