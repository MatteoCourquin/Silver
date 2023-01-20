<template>
  <div class="wrapper-header">
    <header>
      <p class="logo">SIL:VER</p>
      <nav>
        <ul>
          <li><nuxt-link :class="[isDark ? 'links_dark' : 'links_light', 'links']" to="/">Home</nuxt-link></li>
          <li><nuxt-link :class="[isDark ? 'links_dark' : 'links_light', 'links']" to="/shop">Shop</nuxt-link></li>
          <li><nuxt-link :class="[isDark ? 'links_dark' : 'links_light', 'links']" to="/">About</nuxt-link></li>
          <li><nuxt-link :class="[isDark ? 'links_dark' : 'links_light', 'links']" to="/">Contact</nuxt-link></li>
        </ul>
      </nav>
    </header>
    <div :class="[isDark ? 'header-line_dark' : 'header-line_light' ,'header-line']"></div>
  </div>
</template>

<script>

export default {
  name: 'Header',
  props: {
    isDark: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {};
  },
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
  width: 0;
  height: 1px;
  background: $color-white;
  position: absolute;
  bottom: 0;
  left: 0;
}
.header-line_dark{
  background: $color-black;
}
.header-line_light{
  background: $color-white;
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
