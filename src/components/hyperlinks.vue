<template>
  <div class="links-container">
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://source.unsplash.com/zni0zgb3bkQ"></hyperlink>
    <hyperlink title="Contacts" href="https://contacts.google.com/" image="https://source.unsplash.com/ZGyaL6QL7VE"></hyperlink>
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r"></hyperlink>
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://source.unsplash.com/ZGyaL6QL7VE"></hyperlink>
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://picsum.photos/200/200/?random"></hyperlink>
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://picsum.photos/200/200/?random"></hyperlink>
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://picsum.photos/200/200/?random"></hyperlink>
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://picsum.photos/200/200/?random"></hyperlink>
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
