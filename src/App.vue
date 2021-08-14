<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  components: {
    Header
  }
}
</script>

<style lang="scss">
  @font-face {
    font-family: "Helvetica";
    src: local("Helvetica"),
    url(assets/Helvetica.ttf) format("truetype");
  }
  body {
    margin:0;
    padding: 0;
    background-image: url("assets/bg.jpg");
    width:100%;
    min-height: 100vh;
    font-family: Helvetica;
    overflow: auto;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .glide {
    padding: 0 20px 0 35px;
    position: relative;
    .glide__slides {
      padding: 20px 0;
      margin: 0;
    }
    .glide__slide {
      margin: 0 10px;
      cursor: pointer;
      &:hover {
        transform: scale(1.05);
        margin: 0 10px;
      }
    }
    div[data-glide-el='controls'] {
      position: absolute;
      right: 50px;
      top: 40%;
      z-index: 10;
      .books_slider__arrow {
        cursor: pointer;
      }
    }
  }

</style>
