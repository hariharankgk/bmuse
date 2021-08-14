<template>
  <div class="banner">
      <h1 class="banner__title">Bookshelf &amp; Book Racks</h1>
      <p class="banner__description">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
  </div>
</template>

<script>
export default {
  name: 'Banner',
}
</script>

<style scoped lang="scss">
    .banner {
        @media (min-width: 768px) {
            width: 30%;
        }
        .banner__title {
            font-size: 64px;
            font-weight: 100;
            font-stretch: normal;
            font-style: normal;
            line-height: 1.125;
            letter-spacing: normal;
            color: #fff;
            padding-left: 10px;
            margin: 0 0 16px;
            @media (min-width: 768px) {
                padding-left: 50px;
            }
        }

        .banner__description {
            font-size: 16px;
            font-weight: 300;
            font-stretch: normal;
            font-style: normal;
            line-height: 1.38;
            letter-spacing: .4px;
            color: #fff;
            margin: 0;
            max-width: 460px;
            padding-left: 10px;
            @media (min-width: 768px) {
                padding-left: 50px;
            }
        }
        
    }
</style>
