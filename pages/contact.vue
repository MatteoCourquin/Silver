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
        .to('.line-horizontal-contact', { width: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-veritcal-contact-image', { height: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-horizontal-contact-infos', { width: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.line-veritcal-contact-infos', { height: '100%', duration: 4, ease: 'power4.out' }, '-=4')
        .to('.text-1', { y: '0', duration: 2, ease: 'power4.out' }, '-=3')
        .to('.text-2', { y: '0', duration: 4, ease: 'power4.out' }, '-=3')
        .to('.img-wrapper', { y: '0', duration: 2, ease: 'power4.out' }, '-=3.3')
        .to('.infos_1', { x: '0', duration: 2, ease: 'power4.out' }, '-=3')
        .to('.infos_2', { x: '0', duration: 2, ease: 'power4.out' }, '-=2.8')
        .to('.infos_3', { x: '0', duration: 2, ease: 'power4.out' }, '-=2.8')
        .to('.infos_4', { x: '0', duration: 2, ease: 'power4.out' }, '-=2.5')

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