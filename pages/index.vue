<template>
  <div id="wrapper-index" class="wrapper-body">
    <img src='/images/background-body.jpg' class="background-index" />
    <Header :isDark=isDark />
    <div class="wrapper-pages">
      <div class="line-vertical-page line-vertical-page_right"></div>
      <div class="line-vertical-page line-vertical-page_left"></div>
      <div class="line-horizontal-page line-horizontal-page_middle"></div>
      <div class="line-horizontal-page line-horizontal-page_bottom"></div>
      <Hero />
    </div>
  </div>
</template>

<script>
import gsap from 'gsap';

export default {
  name: "IndexPage",
  data() {
    return {
      isDark: false,
    };
  },
  methods: {
    gsapAnimationsLines() {
      const tl = gsap.timeline({ paused: true });


      tl
        .to('.background-index', { opacity: 1, duration: 1.5, ease: 'power4.out' })
        .to('.background-index', { scaleX: 1, scaleY: 1, duration: 6, ease: 'power4.out' }, '-=2')
        .to('.header-line', { width: '100vw', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.line-horizontal-page_middle', { width: '100vw', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.line-hero-decription', { height: '200%', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.line-hero-star', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.line-horizontal-page_bottom', { width: '100vw', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.line-vertical-page_left', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.line-vertical-page_right', { height: '100vh', duration: 4, ease: 'power4.out' }, '-=5')
        .to('.anim-hero-title', { x: '0', duration: 2, ease: 'power4.out' }, '-=3.5')
        .to('.anim-hero-description', { x: '0', duration: 2, ease: 'power4.out' }, '-=3.5')
        .to('.anim-hero-star', { y: '0', duration: 2, ease: 'power4.out' }, '-=3.5')
        .to('.anim-hero-version', { y: '0', duration: 2, ease: 'power4.out' }, '-=3.5')

      tl.play();
    }
  },
  mounted() {
    this.gsapAnimationsLines();
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/style/scss/main.scss';

.background-index {
  position: absolute;
  opacity: 0;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 10% 5%;
  z-index: -1;
  transform: scale(1.5);
}

#wrapper-index {
  min-height: 720px;

  .line-vertical-page {
    background: $color-white;
  }

  .line-horizontal-page {
    position: absolute;
    width: 0;
    height: 1px;
    background: $color-white;
  }

  .line-horizontal-page_middle {
    bottom: calc(360px + 80px);
    right: -80px;

    @include respoXL {
      bottom: calc(250px + 80px);
    }

    @include fullScreen {
      right: calc(((100vw - 1920px) / 2) - ((100vw - 1920px) / 2) * 2);
    }

    @include respoM {
      right: -20px;
    }
  }

  .line-horizontal-page_bottom {
    bottom: 80px;
    left: -80px;

    @include fullScreen {
      left: calc(((100vw - 1920px) / 2) - ((100vw - 1920px) / 2) * 2);
    }

    @include respoM {
      left: -20px;
    }
  }
}
</style>