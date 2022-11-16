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
      <CardComponent
      v-for="(card, index) in cards" :key="index"
      :img="card.thumb" :title="card.series"
      />
    </div>

  </main>
  
</template>


<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

  .container {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
  }

  main {
    background-color: black;
    padding: 1.5rem;
  }
</style>