<script>
export default {
  name: 'CardComponent',
  props: {
    img: String,
    title: String
  },
}
</script>


<template>
  
  <div class="card">

    <div class="img">
      <img :src="img" alt="">
    </div>

    <span class="title">{{title}}</span>

  </div>

</template>


<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

  .card {
    width: calc(100% / 6);
    color: white;
    font-size: $bigger-font-size;
  }

  .title {
    display: inline-block;
    max-width: 75%;
  }

  .img {
    width: 70%;
  }

  img {
    width: 100%;
    aspect-ratio: 1/1;
    object-fit: cover;
    object-position: 0 0;
  }

</style>