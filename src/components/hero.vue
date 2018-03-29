<template>
  <section class="hero is-info">
    <div class="hero-body">
      <div class="container">
        <h1 class="title is-2">{{ title }}</h1>
        <h2 class="subtitle is-3">{{ subtitle }}</h2>
        <slot></slot>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "hero",
  props: {
    title: this.title,
    subtitle: this.subtitle
  },
}
</script>

<style lang="scss">
</style>
