<template>
  <div class="linkbox">
    <h1 class="linkbox__title is-6">{{ title }}</h1>
    <a v-bind:href="href">
      <!-- <figure class="linkbox__image image is-128x128">
        <img src="https://bulma.io/images/placeholders/128x128.png">
      </figure> -->
      <div class="linkbox__color"></div>
    </a>

  </div>
</template>

<script>
export default {
  name: "linkbox",
  props: {
    title: this.title,
    href: this.href,
  },
}
</script>

<style lang="scss">
@import 'node_modules/sass-material-design-colors/palette.scss';

.linkbox {
    width: 160px;
}

.linkbox__title {
    background-color: #757575;
    color: #FAFAFA;
    padding-bottom: 4px;
    text-align: center;
}

.linkbox__color {
  background-color: $blue-400;
  height: 120px;
}
</style>
