
<script>
export default {
  name: 'JumboComponent'
}
</script>

<template>
  <div class="jumbotron">
    <div class="container">
      <p> --> content goes here &lt;-- </p>
    </div>
  </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

  .jumbotron {
    height: 150px;
    background-color: black;
    color: white;
    @include flex('vertical');
  }

  .container {
    display: flex;
    align-items: center;
    font-size: 3rem;
  }
</style>