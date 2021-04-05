<template>
  <nav class="navbar navbar-expand-lg navbar-light box-inner">
    <nuxt-link to="/" class="navbar-brand" exact>
      <strong>Aissam</strong> Bahou.
    </nuxt-link>
    <button
      class="navbar-toggler collapsed"
      type="button"
      data-toggle="collapse"
      data-target="#navbarsExampleDefault"
      aria-controls="navbarsExampleDefault"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="icon-bar top-bar" />
      <span class="icon-bar middle-bar" />
      <span class="icon-bar bottom-bar" />
    </button>

    <div id="navbarsExampleDefault" class="collapse navbar-collapse">
      <ul class="navbar-nav ml-auto">
        <navigation-bar-link link="home">
          Home
        </navigation-bar-link>
        <navigation-bar-link link="about">
          About
        </navigation-bar-link>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavigationBar',
  watch: {
    $route () {
      $('navbarsExampleDefault').collapse('hide')
    }
  }
}
</script>

<style scoped></style>
