<template>
  <div class="wrapper-header">
    <header :class="[isDark ? 'header_dark' : 'header_light']">
      <a href="/" :class="[isDark ? 'logo_dark' : 'logo_light' ,'logo']">SIL:VER</a>
      <nav>
        <ul>
          <li><a :class="[isDark ? 'links_dark' : 'links_light', 'links']" href="/">Home</a></li>
          <li><a :class="[isDark ? 'links_dark' : 'links_light', 'links']" href="/shop">Shop</a></li>
          <li><a :class="[isDark ? 'links_dark' : 'links_light', 'links']" href="/about">About</a></li>
          <li><a :class="[isDark ? 'links_dark' : 'links_light', 'links']" href="/contact">Contact</a></li>
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
  z-index: 50;
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

.header_light{
  background: transparent !important;
}
.header_dark{
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
    font-size: clamp(1.5rem, 5vw, 2.5rem);
  }
  .logo_dark{
    color: $color-black;
  }
  .logo_light{
    color: $color-white;
  }
  nav ul{
    display: flex;
    li {
      margin-left: 20px;
    }
  }
}
</style>
