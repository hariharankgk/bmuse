<template>
  <div class="home">
    <Banner />
    <BookSlider />
  </div>
</template>

<script>
import Banner from '@/components/Banner.vue'
import BookSlider from '@/components/BookSlider.vue'

export default {
  name: 'Home',
  components: {
    Banner,
    BookSlider
  }
}
</script>
