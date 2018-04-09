<template>
  <section class="section logo__container">
    <figure class="container image is-128x128">
      <a href="https://github.com/T0biWan" target="_blank"><img v-bind:src="imagepath"></a>

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

.logo__container {
  margin-top: 0px;
}
</style>
