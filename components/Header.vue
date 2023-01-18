<template>
  <div class="wrapper-header">
    <header>
      <p class="logo">SIL:VER</p>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Shop</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
    </header>
    <div class="header-line"></div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped lang="scss">

@import '~/assets/style/scss/main.scss';

.wrapper-header{
  z-index: 999;
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  padding: 0 80px;
  @include respoM{
    padding: 0 20px;
  }
}
.header-line{
  width: 100vw;
  height: 1px;
  background: $color-white;
  position: absolute;
  bottom: 0;
  left: 0;
}
header {
  height: 80px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1920px !important;
  padding: 0 clamp(20px, 2vw, 40px);
  .logo {
    font-family: $font-new-york;
    color: $color-white;
    font-size: clamp(1.5rem, 5vw, 2.5rem);
  }
  nav ul{
    display: flex;
    li {
      margin-left: 20px;
    }
  }
}
</style>
