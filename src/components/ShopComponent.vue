
<script>
export default {
  name: 'ShopComponent',
  data(){
    return {
      menuItems: [
        {
        text: 'DIGITAL COMICS',
        img: 'buy-comics-digital-comics.png'
      },
        {
        text: 'DC MERCHANDISE',
        img: 'buy-comics-merchandise.png'
      },
        {
        text: 'SUBSCRIPTION',
        img: 'buy-comics-subscriptions.png'
      },
        {
        text: 'COMIC SHOP LOCATOR',
        img: 'buy-comics-shop-locator.png'
      },
        {
        text: 'DC POWER VISA',
        img: 'buy-dc-power-visa.svg'
      },
    ]
    }
  }
}
</script>

<template>
  <main>
    <div class="container">
      <div class="menu">

        <div class="menu-item"
        v-for="(item, index) in menuItems"
        :key="index"
        >
            <img :src= "`../../vue-dc-comics-1/img/${item.img}`" alt="">
          <span>{{item.text}}</span>
        </div>

      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

img, svg {
  width: 70px;
}
main {
  background-color: $accent-color;
  height: 200px;
  @include flex();
}

.menu{
  height: inherit;
  @include flex();
  .menu-item {
    padding: 0 25px;
    @include flex();
    color: white;
    span {
      padding: 0 15px;
    }
  }
}


</style>