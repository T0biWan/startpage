<template>
  <div class="links-container">
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="src/assets/img/hope-house-press-127593-unsplash.jpg"></hyperlink>
    <hyperlink title="Contacts" href="https://contacts.google.com/" image="src/assets/img/nik-macmillan-309702-unsplash.jpg"></hyperlink>
    <hyperlink title="YouTube" href="https://www.youtube.com" image="src/assets/img/ariel-domenden-583207-unsplash.jpg"></hyperlink>
    <hyperlink title="imgur" href="https://imgur.com/" image="src/assets/img/brooke-lark-609907-unsplash.jpg"></hyperlink>

    <hyperlink title="Disroot" href="https://apps.disroot.org/" image="src/assets/img/oscar-nord-588057-unsplash.jpg"></hyperlink>
    <hyperlink title="whatthecommit" href="http://whatthecommit.com/" image="src/assets/img/simon-abrams-286276-unsplash.jpg"></hyperlink>
    <hyperlink title="RegEx" href="https://regex101.com/" image="src/assets/img/chris-ried-532181-unsplash.jpg"></hyperlink>
    <hyperlink title="JSON" href="https://jsoneditoronline.org/" image="src/assets/img/andrew-neel-218073-unsplash.jpg"></hyperlink>

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
