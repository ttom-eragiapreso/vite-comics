
<script>
export default {
  name: 'FooterBottomComponent'
}
</script>

<template>

  <footer>
    <div class="container">
      <span class="sign-up">SIGN-UP NOW!</span>
      <span class="follow">FOLLOW US</span>
      <div class="socials">
        <a href="#"><img src="../../vue-dc-comics-1/img/footer-facebook.png" alt="Facebook"></a>
        <a href="#"><img src="../../vue-dc-comics-1/img/footer-twitter.png" alt="Twitter"></a>
        <a href="#"><img src="../../vue-dc-comics-1/img/footer-youtube.png" alt="Youtube"></a>
        <a href="#"><img src="../../vue-dc-comics-1/img/footer-pinterest.png" alt="Pinterest"></a>
        <a href="#"><img src="../../vue-dc-comics-1/img/footer-periscope.png" alt="Periscope"></a>
      </div>
    </div>
  </footer>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

.container {
  display: flex;
  align-items: center;
  .follow {
    margin-left: auto;
    color: $accent-color;
    font-size: $bigger-font-size;
    font-weight: 600;
    padding: 0 25px;
  }
  .sign-up {
    color: white;
    font-size: $bigger-font-size;
    border: 2px solid $accent-color;
    padding: 1rem;
  }

  .socials a {
    padding: 0 15px;
  }
}
footer{
  background-color: #303030;
  height: 250px;
}
</style>