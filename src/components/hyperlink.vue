<template>
  <a v-bind:href="href" target="_blank">
    <div class="banner__container hyperlink-container">
      <template v-if="image"><img class="hyperlink-content__filler" v-bind:src="image"></template>
      <template v-else><div class="hyperlink-content__filler random-color"></div></template>
      <div class="banner__content">
        <h1 class="hyperlink-content__title">{{title}}</h1>
      </div>
    </div>
  </a>
</template>

<script>
export default {
  name: "hyperlink",

  props: {
    title: this.title,
    href: this.href,
    image: this.image,
  },
}
</script>

<style lang="scss">
  @import '../../node_modules/sass-material-design-colors/palette.scss';
  @import 'src/assets/css/random_color.scss';

  .banner__container {
      position: relative;
  }

  .banner__container .banner__content {
      position: absolute; /* Position the background text */
      top: 0;
      background: rgba(0, 0, 0, 0.5); /* Black background with 0.5 opacity */
      width: 100%;
      padding: 0.7vw;
  }

  .hyperlink-container {
    width: 11vw;
    height: 11vw;
    margin-bottom: 2.2vw;
  }

  .hyperlink-content__title {
      text-align: center;
      font-size: 1.3rem;
      font-weight: 400;

      color: $grey-300;
  }

  .hyperlink-content__filler {
      width: 11vw;
      height: 11vw;
      // opacity: 0.75;
  }

  .random-color {
      background-color: $random-color;
  }
</style>
