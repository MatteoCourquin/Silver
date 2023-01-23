<template>
  <div class="wrapper-hero">
    <div class="hero">
      <div class="hero-wrapper-title-description">
        <div class="hero-description">
          <div class="line-hero-decription"></div>
          <div class="anim-hero-description">
            <p>
              Mixes of silver and solid gold, giving you gorgrous two-tones
              designs that go from day to night
            </p>
          </div>
        </div>
        <div class="hero-title">
          <div class="anim-hero-title">
            <h1 class="flag-element">SILVER & GOLD <br />STORIES</h1>
          </div>
        </div>
      </div>
      <div class="hero-version">
        <div class="anim-hero-version">
          <h2 class="flag-element">VOL.01</h2>
        </div>
      </div>
      <div class="hero-star-wrapper">
        <div class="line-hero-star"></div>
        <div class="hero-star">
          <div class='anim-hero-star'>
            <img class="anim-rotate" src="~/assets/images/icons/star-4.svg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped lang="scss">
@import '~/assets/style/scss/main.scss';

.wrapper-hero {
  width: 100%;
  height: 100vh;
  overflow: hidden;

  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  p,
  span {
    color: $color-white;
  }

  .hero {
    display: grid;
    height: 100%;
    grid-template-columns: 1fr 200px;
    grid-template-rows: 1fr 360px 80px;
    
    @include respoXL {
      grid-template-rows: 1fr 250px 80px;
      grid-template-columns: 1fr 150px;
    }
  }
}

.hero-version {
  display: flex;
  justify-content: center;
  align-items: center;
  grid-column: 2 / 3;
  grid-row: 2 / 3;
  writing-mode: vertical-rl;
  text-orientation: mixed;
  overflow: hidden;

  .anim-hero-version {
    transform: translateY(-200%);
  }
}

.hero-star-wrapper {
  display: flex;
  position: relative;
  justify-content: center;
  align-items: flex-end;
  grid-column: 2 / 3;
  grid-row: 1 / 2;

  .line-hero-star {
    position: absolute;
    top: 80px;
    left: 0;
    height: 0;
    width: 1px;
    background: $color-white;
  }

  .hero-star {
    overflow: hidden;
    width: 100%;
    aspect-ratio: 1 / 1;
    display: flex;
    justify-content: center;
    align-items: center;

    .anim-hero-star {
      transform: translateY(200%);
      width: 80px;
    }
  }
}

.hero-wrapper-title-description {
  display: flex;
  grid-row: 2/3;

  @include respoM {
    grid-row: 2/3;
    flex-direction: column;
  }

  .hero-description {
    padding: clamp(50px, 5vw, 100px);
    width: 30%;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    color: $color-white;

    @include respoXL {
      width: 50%;
    }

    .anim-hero-description {
      transform: translateX(-200%);
    }

    .line-hero-decription {
      height: 0;
      width: 1px;
      position: absolute;
      top: 0;
      right: 0;
      background: $color-white;
    }

  }

  .hero-title {
    width: 80%;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;

    .anim-hero-title {
      transform: translateX(-200%);
    }
  }
}
</style>
