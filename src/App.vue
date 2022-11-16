
<script>
import HeaderComponentVue from './components/HeaderComponent.vue';
import JumboComponentVue from './components/JumboComponent.vue';
import ShopComponentVue from './components/ShopComponent.vue';
import FooterTopComponentVue from './components/FooterTopComponent.vue';
import FooterBottomComponentVue from './components/FooterBottomComponent.vue';
import ComicsComponentVue from './components/ComicsComponent.vue';
export default {
  name: 'App',
  components: {
    HeaderComponentVue,
    JumboComponentVue,
    ShopComponentVue,
    FooterBottomComponentVue,
    FooterTopComponentVue,
    ComicsComponentVue
  },

  data(){
    return {

    }
  },

  methods: {

  }
}
</script>

<template>
  <HeaderComponentVue/>
  <JumboComponentVue/>
  <ComicsComponentVue/>
  <ShopComponentVue/>
  <footer-top-component-vue/>
  <footer-bottom-component-vue/>
  
</template>

<style lang="scss">
@use './styles/general.scss';

</style>