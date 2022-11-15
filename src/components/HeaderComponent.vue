
<script>
export default {
  name: 'HeaderComponent',
  data(){
    return {
      menuItems: [
         {
        text: 'CHARACTERS',
        href: '#',
        current: false
      },
         {
        text: 'COMICS',
        href: '#',
        current: true
      },
         {
        text: 'MOVIES',
        href: '#',
        current: false
      },
         {
        text: 'TV',
        href: '#',
        current: false
      },
         {
        text: 'GAMES',
        href: '#',
        current: false
      },
         {
        text: 'COLLECTIBLES',
        href: '#',
        current: false
      },
         {
        text: 'VIDEOS',
        href: '#',
        current: false
      },
         {
        text: 'FANS',
        href: '#',
        current: false
      },
         {
        text: 'NEWS',
        href: '#',
        current: false
      },
         {
        text: 'SHOP',
        href: '#',
        current: false
      },
    ]
    }
  }

}
</script>

<template>

  <header>
    <div class="container">
      <div class="logo">
        <img src="../public/dc-logo.png" alt="Logo DC">
      </div>
      <div class="menu">
        <ul>
          <li
          v-for="(item, index) in menuItems"
          :key="index"
          :class="{'active' : item.current}"
          ><a :href="item.href">{{item.text}}</a></li>
        </ul>
      </div>
    </div>
  </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;


  header {
    height: 250px;
    @include flex();
    justify-content: space-between;
  }

</style>