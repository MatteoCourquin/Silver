<template>
  <div class="wrapper-shop">
    <div class="shop">
      <div class="shop-top">
        <div class="line-horizontal-shop-middle"></div>
        <div class="wrapper-shop-description">
          <div class="shop-description-title">
            <h1 class="title-anim title-anim-1">SHINE AND SPARKLES</h1>
          </div>
          <div class="shop-description">
            <div class="line-horizontal-description-top"></div>
            <p class="text-anim text-anim-1">Are earrings also an absolute must-have for you?</p>
            <div class="line-vertical-divider"></div>
            <NuxtLink to="/shop" class="links-array text-anim text-anim-2">Shop Now<svg id="Calque_1" data-name="Calque 1"
                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 277.24 546.58" width="1rem" height="1rem">
                <polyline class="cls-1" fill="transparent" stroke="#000" stroke-width="40"
                  points="2.48 2.47 272.3 273.29 2.48 544.11" />
              </svg></NuxtLink>
          </div>
        </div>
        <div class="wrapper-shop-image">
          <div class="line-vertical-shop-image line-vertical-shop-1"></div>
          <img class="image-shop-anim-1" src='/images/shop/illustration1.jpg' />
        </div>
      </div>
      <div class="shop-bottom">
        <div class="wrapper-shop-image">
          <div class="line-vertical-shop-image line-vertical-shop-2"></div>
          <img class="image-shop-anim-2" src='/images/shop/illustration2.jpg' />
        </div>
        <div class="wrapper-shop-description">
          <h2 class="title-anim title-anim-2">NECKLESS</h2>
          <p class="text-anim text-anim-3">To highlight your <br>neck shape and curves</p>
          <div class="wrapper-star">
            <img class="anim-rotate" src="/images/icons/star-8.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Shop',
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped lang="scss">
@import '~/assets/style/scss/main.scss';

.wrapper-shop-description {
  overflow: hidden;

  .title-anim {
    transform: translateX(-110%);
  }

  .text-anim {
    opacity: 0;
  }
}


.wrapper-shop-image {
  padding: 10px;
  position: relative;
  height: 100%;
  overflow: hidden;

  .image-shop-anim-1 {
    transform: translate(110%, 110%);
  }

  .image-shop-anim-2 {
    transform: translateY(110%);
  }
}


.line-vertical-shop-image {
  position: absolute;
  top: 0;
  width: 1px;
  height: 0;
  background-color: $color-black;
}

.line-vertical-shop-1 {
  left: 0;
}

.line-vertical-shop-2 {
  right: 0;
}


img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.image-shop-anim-1 {
  border-radius: 50% 0 0 0;
}

.image-shop-anim-2 {
  border-radius: 300px 300px 0 0;
}

.wrapper-shop {
  padding-top: 80px;

  h1,
  h2 {
    font-size: clamp(2.5rem, 8vw, 8rem);
    line-height: clamp(2.5rem, 8vw, 8rem);
  }

  .shop {
    height: calc(100vh - 80px);
    display: grid;
    grid-template-rows: 2fr 2fr;
  }

  .shop-top {
    display: grid;
    grid-template-columns: 3fr 2fr;
    position: relative;

    .line-horizontal-shop-middle {
      position: absolute;
      bottom: 0;
      width: 0;
      height: 1px;
      background-color: $color-black;
    }

    .wrapper-shop-description {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      p {
        padding: 0 20px;
      }

      .shop-description-title {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 70%;
        padding: 0 5vw;
      }

      .shop-description {
        height: 30%;
        max-height: 200px;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        position: relative;
        overflow: hidden;

        @include respoXL {
          p {
            width: 50%;
          }
        }

        .line-horizontal-description-top {
          position: absolute;
          top: 0;
          right: 0;
          width: 0;
          height: 1px;
          background-color: $color-black;
        }

        .line-vertical-divider {
          transform: translateY(-100%);
          bottom: 0;
          width: 1px;
          height: 100%;
          background: $color-black;
        }
      }

    }
  }

  .shop-bottom {
    height: 100%;
    display: grid;
    grid-template-columns: 2fr 4fr;

    .wrapper-shop-description {
      padding: 0 5vw;
      display: flex;
      justify-content: center;
      flex-direction: column;
      position: relative;

      p {
        line-height: 1.6rem;
      }

      .wrapper-star {
        padding: 20px;
        width: 120px;
        height: 120px;
        position: absolute;
        bottom: 0;
        right: 0;
        border-top: 1px solid $color-black;
        border-left: 1px solid $color-black;
      }
    }
  }
}
</style>
