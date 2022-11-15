
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
  },
  methods: {
    activate(item){
      this.menuItems.forEach(item => item.current = false);
      item.current = true
    }
  }

}
</script>

<template>

  <header>
    <div class="container">

      <div class="logo">
        <img src="../../vue-dc-comics-1/img/dc-logo.png" alt="Logo DC">
      </div>

        <ul class="menu">
          <li
          v-for="(item, index) in menuItems"
          :key="index"
          :class="{'active' : item.current}"
          @click="activate(item)"
          ><a :href="item.href">{{item.text}}</a></li>
        </ul>

    </div>
  </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

  a {
    color: inherit;
  }

  header {
    height: 180px;
    padding: 0 2.5rem;
  }

  .container {
    @include flex('vertical');
    justify-content: space-between;
    height: 100%
  }

  .menu {
    @include flex();
    height: 100%;
    li {
      height: 100%;
      @include flex();
      padding: 0 15px;
      font-size: $bigger-font-size;
      &:hover a {
        color: $accent-color;
      }
      &.active {
        color: $accent-color;
        box-shadow: inset 0px -7px 0 0px $accent-color;
      }
    }
  }

</style>