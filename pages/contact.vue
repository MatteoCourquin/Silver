<template>
  <div id="wrapper-contact" class="wrapper-body">
    <Header :isDark=isDark />
    <div class="wrapper-pages">
      <div class="line-vertical-page line-vertical-page_right"></div>
      <div class="line-vertical-page line-vertical-page_left"></div>
      <Contact />
    </div>
  </div>
</template>

<script>
import gsap from 'gsap';

export default {
  name: 'contact',
  data() {
    return {
      isDark: true,
    };
  },
  methods: {
    gsapAnimationsLines() {
      const tl = gsap.timeline({ paused: true });

      tl
        .to('.header-line', { width: '100vw', duration: 4, ease: 'power4.out' })
        .to('.line-vertical-page_left', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-vertical-page_right', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=4')

      tl.play();
    }
  },
  mounted() {
    this.gsapAnimationsLines();
  }
}

</script>

<style scoped lang='scss'>
@import '~/assets/style/scss/main.scss';

#wrapper-contact {
  .line-vertical-page {
    background: $color-black;
  }
}
</style>