<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style lang="scss">
$fa-font-path: "~font-awesome/fonts";
@import '~font-awesome/scss/font-awesome';
@import '~bulma/sass/utilities/_all';
@import "~bulma";
@import "~buefy/src/scss/buefy";
</style>
