<template>
  <div class="about">

    <div class="wrapper-about-titles">
      <div class="about-year about-year_1">
        <span>20</span>
      </div>
      <div class="titles-about">
        <h2>GOLDEN</h2>
        <h2>COLLECTION</h2>
      </div>
      <div class="about-year about-year_2">
        <span>22</span>
      </div>
    </div>

    <div class="about-footer">
      <div class="tile-about">
        <h3>SOAP STORE</h3>
      </div>
      <div class="line-vertical-footer"></div>
      <NuxtLink to="/shop" class="links-array text-anim text-anim-2">Shop Now<svg id="Calque_1" data-name="Calque 1"
          xmlns="http://www.w3.org/2000/svg" viewBox="0 0 277.24 546.58" width="1rem" height="1rem">
          <polyline class="cls-1" fill="transparent" stroke="#000" stroke-width="40"
            points="2.48 2.47 272.3 273.29 2.48 544.11" />
        </svg></NuxtLink>
      <div class="line-vertical-footer"></div>
      <div class="about-star">
        <div class='anim-about-star'>
          <img class="anim-rotate" src="~/assets/images/icons/star-8.svg" alt="">
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
  padding-top: 80px;
  display: grid;
  grid-template-rows: 1fr 150px;
  position: relative;

  .line-vertical-page {
    background: $color-black;
  }

  .wrapper-about-titles {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .about-year,
  .titles-about {
    border-radius: 99999999px;
    border: 1px solid $color-black;
    aspect-ratio: 1/1;
    height: 60%;
    position: absolute;
  }

  .about-year {
    display: flex;
    justify-content: center;
    align-items: center;

    span {
      font-family: $font-new-york;
      color: $color-black;
      font-weight: normal;
      font-size: clamp(2rem, 5vw, 6rem);
    }
  }

  .about-year_1 {
    left: 0;
  }

  .about-year_2 {
    right: 0;
  }

  .titles-about {
    background-image: url('assets/images/about/illustration1.jpg');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
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
    align-items: center;
    justify-content: flex-end;

    .tile-about{
      width: 100%;
      padding: 0 80px;
      h3 {
        font-size: clamp(1rem, 5vw, 2rem);
      }
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
      width: 100%;
    }

    .line-vertical-footer {
      background: $color-black;
      height: 100%;
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
