<template>
  <div class="wrapper-contact">
    <div class="contact-top">
      <h1>CONTACT US</h1>
      <p>natural.soap@gmail.com</p>
      <div class="line-horizontal-contact"></div>
    </div>
    <div class="contact-bottom">
      <div class="contact-bottom-image">
        <div class="line-veritcal-contact-image"></div>
        <div class="img-wrapper">
        </div>
      </div>
      <div class="contact-bottom-wrapper-indos">
        <div class="line-horizontal-contact-infos"></div>
        <div class="line-veritcal-contact-infos"></div>
        <div class="container-infos">
          <h2>ADRESS</h2>
          <div class="infos">
            <p>Vitkin Street 14, Tev-Aviv, Israel</p>
          </div>
        </div>
        <div class="container-infos">
          <h2>PHONE</h2>
          <div class="infos">
            <p>+38 (093) 019 15 50</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped lang="scss">
@import '~/assets/style/scss/main.scss';

.wrapper-contact {
  padding-top: 80px;
  display: grid;
  grid-template-rows: 3fr 2fr;
  height: 100vh;
  overflow: hidden;

  h1 {
    font-size: clamp(2.5rem, 8vw, 8rem);
    line-height: clamp(2.5rem, 8vw, 8rem);
    padding-bottom: 20px;
  }
}

.contact-top {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  .line-horizontal-contact {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 1px;
    background-color: $color-black;
  }
}

.contact-bottom {
  display: grid;
  grid-template-columns: 1fr 2fr;

  .contact-bottom-image {
    width: 100%;
    height: 100% !important;
    padding: 10px 10px 0 10px;
    position: relative;

    .line-veritcal-contact-image {
      position: absolute;
      right: 0;
      bottom: 0;
      width: 1px;
      height: 100%;
      background-color: $color-black;
    }

    .img-wrapper {
      width: 100%;
      height: 100%;
      border-radius: 999px 999px 0 0;
      background: url('/images/background-body.jpg') no-repeat center center;
      background-size: cover;
    }
  }

  .contact-bottom-wrapper-indos {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: center;
    position: relative;

    .line-horizontal-contact-infos {
      position: absolute;
      width: 100%;
      top: 100px;
      height: 1px;
      background-color: $color-black;
    }

    .line-veritcal-contact-infos {
      position: absolute;
      right: 50%;
      width: 1px;
      height: 100%;
      background-color: $color-black;
    }

    .container-infos {
      display: grid;
      grid-template-rows: 100px 1fr;

      h2 {
        height: 100px;
        line-height: 100px;
      }

      .infos {
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }

  }
}
</style>
