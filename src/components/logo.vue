<template>
  <section class="section">
    <figure class="container image is-128x128">
      <img v-bind:src="imagepath">
    </figure>
  </section>
</template>

<script>
export default {
  name: "logo",

  props: {
    imagepath: this.imagepath,
  },
}
</script>

<style lang="scss">
img {
  opacity: 1.0;
}
</style>
