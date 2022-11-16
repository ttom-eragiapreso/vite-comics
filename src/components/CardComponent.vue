<script>
export default {
  name: 'CardComponent',
  props: {
    img: String,
    title: String
  },
  data(){
    return {
 
    }
  }
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
  aspect-ratio: 1/1;
  border: 1px solid white;
  color: white;
  .img {
    width: 100%;
    aspect-ratio: 1/1;
    img {
      width: 100%;
      aspect-ratio: 1/1;
      object-fit: contain;
    }
  }
}

</style>