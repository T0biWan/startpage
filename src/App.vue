<template>
<div id="app">
  <section class="section">
    <div class="container logo-container">
      <img class="logo-container__image" src="./assets/logo/wave-logo-color.png">
    </div>
  </section>

  <section class="section">
    <div class="field has-addons">
      <div class="control has-icons-left">

        <span class="select">
          <select>
            <option>google</option>
            <option>€</option>
            <option>$</option>
            <option>£</option>
          </select>
        </span>

        <span class="icon is-small is-left">
          <i class="fab fa-searchengin"></i>
        </span>
      </div>
      <div class="control is-expanded">
        <input class="input" type="text" placeholder="Find a repository">
      </div>
      <div class="control">
        <a class="button is-info"><i class="fas fa-search"></i></a>
      </div>
    </div>
  </section>

</div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {}
  }
}
</script>

<style>
.logo-container {
  width: 250px
}
</style>
