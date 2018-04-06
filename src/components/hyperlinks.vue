<template>
  <div class="links-container">
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://source.unsplash.com/zni0zgb3bkQ"></hyperlink>
    <hyperlink title="Contacts" href="https://contacts.google.com/" image="https://source.unsplash.com/ZGyaL6QL7VE"></hyperlink>
    <hyperlink title="YouTube" href="https://www.youtube.com" image="https://source.unsplash.com/NmGzVG5Wsg8"></hyperlink>
    <hyperlink title="imgur" href="https://imgur.com/" image="https://source.unsplash.com/Fo5dTm6ID1Y"></hyperlink>

    <hyperlink title="GitHub" href="https://github.com/" image="https://source.unsplash.com/fPkvU7RDmCo"></hyperlink>
    <hyperlink title="whatthecommit" href="http://whatthecommit.com/" image="https://source.unsplash.com/Skf7HxARcoc"></hyperlink>
    <hyperlink title="RegEx" href="https://regex101.com/" image="https://source.unsplash.com/466ENaLuhLY"></hyperlink>
    <hyperlink title="JSON" href="https://jsoneditoronline.org/" image="https://source.unsplash.com/feXpdV001o4"></hyperlink>
  </div>
</template>

<script>
import hyperlink from "./hyperlink.vue"

export default {
  name: "hyperlinks",

  components: {
    hyperlink,
  },
}
</script>

<style lang="scss">
.links-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 2.2vw;
}
</style>
