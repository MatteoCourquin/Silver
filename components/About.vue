<template>
  <div class="about">
    <div class="wrapper-about-titles">
      <div class="about-year about-year_1">
        <span class="anim-about-year-1">20</span>
      </div>
      <div class="titles-about">
        <div class="image-about"></div>
        <h2 class="anim-title-about-1">GOLDEN</h2>
        <h2 class="anim-title-about-2">COLLECTION</h2>
      </div>
      <div class="about-year about-year_2">
        <span class="anim-about-year-2">22</span>
      </div>
    </div>

    <div class="about-footer">
      <div class="tile-about">
        <h3 class="anim-title-about-3">SOAP STORE</h3>
      </div>
      <div class="line-vertical-footer line-vertical-footer_1"></div>
      <div class="link-about">
        <NuxtLink to="/shop" class="links-array anim-title-about-4">Shop Now<svg id="Calque_1" data-name="Calque 1"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 277.24 546.58" width="1rem" height="1rem">
            <polyline class="cls-1" fill="transparent" stroke="#000" stroke-width="40"
              points="2.48 2.47 272.3 273.29 2.48 544.11" />
          </svg></NuxtLink>
      </div>
      <div class="line-vertical-footer line-vertical-footer_2"></div>
      <div class="about-star">
        <div class='anim-about-star'>
          <img class="anim-rotate" src="/images/icons/star-8.svg" alt="">
        </div>
      </div>
      <div class="line-horizontal-footer"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped lang="scss">
@import '~/assets/style/scss/main.scss';

.about {
  height: 100vh;
  width: 100%;
  padding-top: 80px;
  display: grid;
  grid-template-rows: 1fr 150px;
  position: relative;
  overflow: hidden;

  .line-vertical-page {
    background: $color-black;
  }

  .wrapper-about-titles {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
  }

  .about-year,
  .titles-about {
    border-radius: 99999999px;
    border: 1px solid $color-black;
    aspect-ratio: 1/1;
    height: 60%;
    position: absolute;

    .anim-title-about-1 {
      position: absolute;
      top: 0;
      transform: translateY(-50vh);
    }

    .anim-title-about-2 {
      position: absolute;
      bottom: 0;
      transform: translateY(50vh);
    }
  }

  .about-year {
    display: flex;
    justify-content: center;
    align-items: center;

    @media screen and (max-width : 1000px) {
      display: none;
    }

    span {
      font-family: $font-new-york;
      color: $color-black;
      font-weight: normal;
      font-size: clamp(2rem, 5vw, 6rem);
      opacity: 0;

      @media screen and (max-width : 1300px) {
        display: none;
      }
    }

    .anim-about-year-1 {
      transform: translateX(20vh);
    }

    .anim-about-year-2 {
      transform: translateX(-20vh);
    }
  }

  .about-year_1 {
    left: -100vw;
  }

  .about-year_2 {
    right: -100vw;
  }

  .titles-about {
    .image-about {
      background-image: url('/images/about/illustration1.jpg');
      background-position: center;
      background-size: cover;
      background-repeat: no-repeat;
      overflow: hidden;
      border-radius: 9999px;
      width: 100%;
      height: 100%;
      transform: translateY(100vh);
    }

    border: none;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    z-index: 1;

    h2 {
      font-size: clamp(2rem, 5vw, 6rem);
      margin: -30px 0;
    }
  }

  .about-footer {
    position: relative;
    display: flex;
    justify-content: flex-end;
    z-index: 1;
    background: $color-white;

    .tile-about {
      width: 100%;
      padding: 0 80px;
      display: flex;
      align-items: center;

      .anim-title-about-3 {
        transform: translateX(-700px);
      }

      h3 {
        font-size: clamp(1rem, 5vw, 2rem);
      }
    }

    .anim-title-about-4 {
      transform: translateX(-700px);
    }

    .link-about {
      width: fit-content;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .links-array {
      padding: 0 80px;
    }

    .line-horizontal-footer {
      position: absolute;
      top: 0;
      left: 0;
      background: $color-black;
      height: 1px;
      width: 0%;
    }

    .line-vertical-footer {
      background: $color-black;
      height: 0%;
      bottom: 0;
      width: 1px;
    }

    .about-star {
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      aspect-ratio: 1 / 1;
      height: 100%;
      min-width: fit-content;

      .anim-about-star {
        // transform: translateY(200%);
        width: 80px;
      }
    }
  }
}</style>
