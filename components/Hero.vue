<template>
  <div class="wrapper-hero">
    <div class="hero">
      <div class="hero-wrapper-title-description">
        <div class="hero-description">
          <div class="line-hero-decription"></div>
          <p>
            Mixes of silver and solid gold, giving you gorgrous two-tones
            designs that go from day to night
          </p>
        </div>
        <div class="hero-title">
          <h1 class="flag-element">SILVER & GOLD <br />STORIES</h1>
        </div>
      </div>
      <div class="hero-version">
        <h2 class="flag-element">VOL.01</h2>
      </div>
      <div class="hero-star-wrapper">
        <div class="line-hero-star"></div>
        <div class="hero-star">
          <svg
            id="star"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 282.5 282.5"
          >
            <path
              class="cls-1"
              fill="#f4efe8"
              d="M0,141.75c46.88-5.58,94.11-6.8,141.25-7,47.14,.17,94.37,1.39,141.25,7-46.88,5.61-94.11,6.83-141.25,7-47.14-.2-94.37-1.42-141.25-7H0Z"
            />
            <path
              class="cls-1"
              fill="#f4efe8"
              d="M144.5,0c5.58,46.88,6.8,94.11,7,141.25-.17,47.14-1.39,94.37-7,141.25-5.61-46.88-6.83-94.11-7-141.25,.2-47.14,1.42-94.37,7-141.25h0Z"
            />
          </svg>
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
  .hero {
    display: grid;
    height: 100%;
    grid-template-columns: 1fr 200px;
    grid-template-rows: 1fr 360px 80px;
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
}
.hero-star-wrapper {
  display: flex;
  position: relative;
  justify-content: center;
  align-items: flex-end;
  grid-column: 2 / 3;
  grid-row: 1 / 2;
  .line-hero-star{
    position: absolute;
    top: 80px;
    left: 0;
    height: calc(100vh - 80px);
    width: 1px;
    background: $color-white;
  }
  .hero-star {
    width: 100%;
    aspect-ratio: 1 / 1;
    display: flex;
    justify-content: center;
    align-items: center;
    #star {
      width: 80px;
      transform: rotate(965deg);
    }
  }
}
.hero-wrapper-title-description {
  display: flex;
  grid-row: 2/3;
  .hero-description {
    padding: 100px;
    width: 30%;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    color: $color-white;
    .line-hero-decription {
      height: 200%;
      width: 1px;
      position: absolute;
      top: 0;
      right: 0;
      background: $color-white;
    }
  }
  .hero-title {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
