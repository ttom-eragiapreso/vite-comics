
<script>
export default {
  name: 'JumboComponent'
}
</script>

<template>
  <div class="jumbotron">
  </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

  .jumbotron {
    background-image: url(../../vue-dc-comics-1/img/jumbotron.jpg);
    height: 450px;
  }

</style>