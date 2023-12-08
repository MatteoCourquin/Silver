<template>
  <div class="wrapper-desktop-alert">
    <h1>This website is only avaible on Desktop</h1>
    <p>Designed by <a href="https://dribbble.com/TheGlyphStudio" target="_blank">The Glyph Studio</a></p>
  </div>
</template>

<script>

export default {
  name: 'DesktopAlert',
  data() {
    return {};
  },
  methods: {}
}

</script>

<style scoped lang='scss'>
@import '~/assets/style/scss/main.scss';

.wrapper-desktop-alert{
  background-image: url('/images/background-body.jpg');
  background-size: cover;
  background-position: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9999;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  display: none;
  @include respoM {
    display: flex;
  }
  h1{
    color: #fff;
    margin-bottom: 20px;
  }
  p{
    color: #fff;
    padding: 0 20px;
  }
}
  
</style>