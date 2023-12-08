<template>
  <div id="wrapper-shop" class="wrapper-body">
    <Header :isDark=isDark />
    <div class="wrapper-pages">
      <div class="line-vertical-page line-vertical-page_right"></div>
      <div class="line-vertical-page line-vertical-page_left"></div>
      <Shop />
    </div>
  </div>
</template>

<script>

import gsap from 'gsap';

export default {
  name: 'shop',
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
        .to('.line-vertical-divider', { y: 0, duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-vertical-page_left', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-vertical-page_right', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-horizontal-description-top', { width: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-horizontal-shop-middle', { width: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-vertical-shop-1', { height: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-vertical-shop-2', { height: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.image-shop-anim-2', { y: 0, duration: 1.5, ease: 'power4.out' }, '-=3')
        .to('.image-shop-anim-1', { x: '0', y: 0, duration: 1.5, ease: 'power4.out' }, '-=2')
        .to('.title-anim-1', { x: '0', y: 0, duration: 1.5, ease: 'power4.out' }, '-=2')
        .to('.title-anim-2', { x: '0', y: 0, duration: 1.5, ease: 'power4.out' }, '-=2')
        .to('.text-anim-1', { opacity: 1, duration: 1.5, ease: 'power4.out' }, '-=1')
        .to('.text-anim-2', { opacity: 1, duration: 1.5, ease: 'power4.out' }, '-=1.2')
        .to('.text-anim-3', { opacity: 1, duration: 1.5, ease: 'power4.out' }, '-=1.4')

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

#wrapper-shop {
  .line-vertical-page {
    background: $color-black;
  }
}
</style>