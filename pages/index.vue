<template>
  <div id="wrapper-index" class="wrapper-body">
    <div class="wrapper-pages">
      <div class="line-vertical-page line-vertical-page_right"></div>
      <div class="line-vertical-page line-vertical-page_left"></div>
      <div class="line-horizontal-page line-horizontal-page_middle"></div>
      <div class="line-horizontal-page line-horizontal-page_bottom"></div>
      <Header />
      <Hero />
    </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Hero from '~/components/Hero.vue';

export default {
    name: "IndexPage",
    components: { Hero, Header }
}
</script>

<style lang="scss">

@import '~/assets/style/scss/main.scss';

</style>