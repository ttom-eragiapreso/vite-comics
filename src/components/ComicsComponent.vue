<script>
import CardComponent from './CardComponent.vue';
import cards from '../../vue-dc-comics-2/dc-comics.json'

export default {
  name: 'ComicsComponent',
  data(){
    return {
      cards
    }
  },
  components: {
    CardComponent
  }

}
</script>

<template>
  <main>

    <div class="container">
      <span class="current-series">current series</span>

      <CardComponent
      v-for="(card, index) in cards" :key="index"
      :img="card.thumb" :title="card.series"
      />
    </div>

    <div class="btn-container">
      <span class="load-more">load more</span>
    </div>
    
  </main>
  
</template>


<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

  .container {
    display: flex;
    flex-wrap: wrap;
    padding: 1rem;
    position: relative;

  }

  main {
    background-color: black;
    padding: 1.5rem;
  }

  .current-series {
    @include spanAccent($accent-color);
    position: absolute;
    top: -52px;
    left: 0px;
  }

  .btn-container {
    text-align: center;
  }

  .load-more {
    @include spanAccent($accent-color);
    font-size: 1rem;
    padding: 10px 40px;
  }
</style>