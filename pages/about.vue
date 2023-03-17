<template>
  <div id="wrapper-about" class="wrapper-body">
    <Header :isDark=isDark />
    <div class="wrapper-pages">
      <div class="line-vertical-page line-vertical-page_right"></div>
      <div class="line-vertical-page line-vertical-page_left"></div>
      <About />
    </div>
  </div>
</template>

<script>
import About from '~/components/About.vue';
import Header from '~/components/Header.vue';
import gsap from 'gsap';

export default {
  name: 'about',
  components: {
    Header,
    About
  },
  data() {
    2
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
        .to('.line-horizontal-footer', { width: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-vertical-footer_1', { height: '100%', duration: 4, ease: 'power4.out' }, '-=3.3')
        .to('.line-vertical-footer_2', { height: '100%', duration: 4, ease: 'power4.out' }, '-=3.4')
        .to('.anim-title-about-1', {y: '0', duration: 2, ease: 'power4.out' }, '-=4')
        .to('.anim-title-about-2', {y: '0', duration: 2, ease: 'power4.out' }, '-=4')
        .to('.image-about', {y: '0', duration: 2, ease: 'power4.out' }, '-=4')
        .to('.anim-about-year-1', {x: '0', opacity: '1', duration: 2, ease: 'power4.out' }, '-=2')
        .to('.anim-about-year-2', {x: '0', opacity: '1', duration: 2, ease: 'power4.out' }, '-=2')
        .to('.about-year_1', {left: '0', opacity: '1', duration: 3, ease: 'power4.out' }, '-=3.4')
        .to('.about-year_2', {right: '0', opacity: '1', duration: 3, ease: 'power4.out' }, '-=3.4')
        .to('.anim-title-about-3', {x: '0', opacity: '1', duration: 3, ease: 'power4.out' }, '-=3.4')
        .to('.anim-title-about-4', {x: '0', opacity: '1', duration: 3, ease: 'power4.out' }, '-=3.4')
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

#wrapper-about {
  .line-vertical-page {
    background: $color-black;
  }
}
</style>